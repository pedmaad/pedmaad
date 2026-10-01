# Install the personal neon portrait profile

Upload README.md, hero.svg, skills.svg, donations.svg, github-live.svg and latest-repo.svg into the existing public pedmaad/pedmaad repository. The two custom data cards use relative paths and display immediately. avatar.svg is included as a standalone reusable portrait; hero.svg already contains it. Both SVGs embed the portrait pixels directly, so they need no external image file to display. portrait.png is the reusable transparent source image, and portrait-prompt.txt contains the prompt used with the built-in image generation tool.

The .github files must reach their exact paths too. Selecting only the top-level SVGs and README in an upload does not install the workflow. If folder upload is awkward, use **Add file → Create new file** and copy these files from the ZIP, in this order:

1. .github/scripts/render-profile.py
2. .github/scripts/speed-up-snake.py
3. .github/workflows/snake.yml

Create the workflow last so its first run has both scripts available. Then open **Actions → Profile cards and contribution snake → Run workflow**. You should see this named workflow; if the Actions page is empty, the workflow file is still missing.

Once successful, the job refreshes github-live.svg and latest-repo.svg on the default branch and publishes the contribution snake on output. The README's custom cards use the root files; the snake uses output. GitHub may cache images briefly.

The root data cards are genuine initial snapshots. The workflow commits updates only to those two generated root cards, using the built-in GITHUB_TOKEN with contents-write permission. It also publishes output. No extra account or personal access token is needed.

Custom cards refresh daily at 03:17 UTC, after profile source changes, or on a manual workflow run. Changes in another project repository appear at the next daily/manual refresh. They are snapshots, not a real-time feed. GitHub can delay scheduled runs and disable schedules in inactive public repositories.

The totals exclude repositories you forked. Stars and forks count those received on your original public repositories. The latest panel selects your most recently pushed original project, excluding this profile repository when another original exists. Its date is the latest source commit on its default branch; automatic card-refresh commits from this workflow are skipped, so scheduled refreshes do not masquerade as source changes. Until you have another original repository, it honestly shows the profile README.

The four connected panels have separate roles: identity, practice, GitHub totals, and repository history. They share a visual rail and palette. The header portrait is based on your actual photos, primarily the close-up in the black leather jacket. The generated illustration preserves your hairstyle and facial features, with neon contour lines and selective mesh. SMIL supplies moving scan light, subtle vertical drift, illuminated mesh junctions, orbiting points and side meters. This is a photo-derived illustration with animated lighting, not a reconstructed 3D face.

Portrait scan: 0.75 seconds; signal paths: 0.7 seconds; light pulses: 0.65–0.8 seconds; gentle drift: 1.2 seconds; orbit: 2 seconds. The border runs in 1.5 seconds, and panel pulses use 0.6 seconds. Typing uses 700 milliseconds with a 250-millisecond pause. The workflow shortens the generated contribution snake's animation clocks by four, preserving its contribution data. Run the updated workflow once to publish the animated live cards and snake.

All lower custom panels now have visible motion: moving skill tracks, network packets, lab bubbles, rotating metric icons, orbiting points, number-color shimmer, and a moving commit trail. Donation outlines also have moving highlights. Names, skill ratings, GitHub counts, and commit dates stay fixed; the motion is decorative. These additions use small SMIL loops with no filters, JavaScript, or CSS.

BTC, ETH and USDT fields remain invalid demo addresses. Replace them and specify the USDT network before adding payment links or QR codes.

The live language donut remains linked, as requested; it will show available public code data when the service has it. The shared stats service can fail temporarily; its stats card now uses the simpler period-based commit query rather than the all-time query. Layout height depends on browser width; the compact layout is designed for GitHub desktop widths.

Data and action references: [GitHub repository API](https://docs.github.com/en/rest/repos/repos), [scheduled workflow behavior](https://docs.github.com/en/actions/reference/workflows-and-actions/events-that-trigger-workflows#schedule), [Platane/snk](https://github.com/Platane/snk), [GitHub Pages publishing action](https://github.com/crazy-max/ghaction-github-pages), [shared stats-service limits](https://github.com/anuraghazra/github-readme-stats#important-notices).
