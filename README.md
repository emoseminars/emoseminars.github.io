# EMO Talks website

Source for the EMO Talks website at <https://emoseminars.github.io/>.

Each Markdown file in `_events/` supplies the upcoming-talk card, its semester
table row, and its talk-information page.

## Add a talk

1. Copy `_events/example_talk.md`.
2. Rename the copy to a descriptive filename such as
   `_events/speaker-last-name-topic.md`.
3. Replace the example values, preserving the opening and closing `---` lines.
4. Preview the site locally.
5. Commit and push the change once deployment is configured.

The exact `_events/example_talk.md` file is an organizer template and is
excluded from the published site.

### Date, time, and semester

```yaml
talk_date: "2026-09-23"
start_time: "3:00 PM"
duration_minutes: 60
semester: fall-2026
```

Use `YYYY-MM-DD` for the date and `h:mm AM/PM` for the time, quoting both
values. Times are interpreted as U.S. Eastern time through
`America/New_York`, which handles EST and EDT automatically; do not enter a UTC
offset.

Semester keys use `term-year`, for example `fall-2026`, `spring-2027`, or
`summer-2027`. The homepage creates and orders semester sections automatically.

The upcoming card is selected when Jekyll builds the site. A talk remains
upcoming until its start time plus `duration_minutes` has passed. Passage of
time alone does not rebuild a static site; the normal post-talk recording update
and push will refresh the selection.

### Links and optional fields

- `speaker_url` links the speaker's name to a personal or institutional page.
- Fill in either `registration_url` or `join_url`, not both. Registration is the
  recommended public default. Never commit a host-only link, start link,
  password, or another private credential; waiting-room settings live in Zoom.
- Add the YouTube URL to `recording_url` after a talk. The schedule then shows
  `[Video]` after its title.
- `abstract` and `bio` support Markdown.
- Leave unavailable optional fields blank so the layout hides them cleanly.

Keep ordinary text values such as `title`, `speaker`, and `affiliation` quoted.
When pasting under `abstract: >-` or `bio: >-`, keep every content line indented
by two spaces, as shown in the template.

### Speaker images

Speaker images are optional. Create `assets/images/speakers/` when the first
image is needed, put local images there, and configure them like this:

```yaml
image: /assets/images/speakers/jane-doe.jpg
image_alt: Portrait of Jane Doe
```

Use meaningful alt text for every real headshot. Leave both fields blank when
no image is available.

### Rescheduling, cancellation, and postponement

For a reschedule, update `talk_date`, `start_time`, and `duration_minutes` in the
existing file. Update `semester` too only when the new date crosses into another
term. Normally keep:

```yaml
status: scheduled
```

Use `status: cancelled` or `status: postponed` only when a public notice is
helpful. Those talks remain labelled in their semester table and are skipped by
the upcoming selector. Delete the Markdown file instead to remove an entry
silently.

## Change the logo

`icon` in `_config.yml` controls the square header icon and favicon. Replace
`assets/images/emo-talks-icon.svg` with the official square mark, or change the
configured path.

For a wide wordmark, set `header_logo.path` in `_config.yml`. Set
`includes_title: true` when the image already contains “EMO Talks”; otherwise
use `false` so the text title remains visible.

## Preview locally

Local Ruby is optional. GitHub Actions performs the authoritative build after
each push. If Ruby is already installed and a local preview is useful, use the
version listed in `.ruby-version` and run:

```sh
bundle install
bundle exec jekyll serve
```

Open <http://127.0.0.1:4000/> and stop the server with `Ctrl-C`.

For a production build:

```sh
JEKYLL_ENV=production bundle exec jekyll build
```

Do not commit the generated `_site/` directory.

## Publishing

The workflow in `.github/workflows/pages.yml` builds with GitHub's official
Jekyll Pages action on pushes to `main`, verifies the generated output, and
deploys it. It can also be run manually from the repository's Actions tab.
Pull requests run the build checks without deploying.

After the first push, an organization owner must open **Settings → Pages** and
set **Source** to **GitHub Actions**. Build or deployment errors appear in the
repository's **Actions** tab.

This downloaded folder is not yet connected to GitHub. The Codex GitHub
connection must be granted access to the `emoseminars` organization before it
can publish this source directly.

The public user/organization repository must be named
`emoseminars/emoseminars.github.io`, with an empty `baseurl`.

## Licensing

The MIT licenses apply only to the website software derived from the upstream
templates. EMO Talks site content, speaker-contributed materials, recordings,
images, and branding are not licensed under MIT and remain with their respective
rights holders. See `LICENSE.md` for the complete scope and notices.

## Credits

Derived from [mjungmath/jekyll-seminar](https://github.com/mjungmath/jekyll-seminar)
and [Minima](https://github.com/jekyll/minima).
