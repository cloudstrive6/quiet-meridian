# quiet-meridian

Scheduled cross-poster. A PC publisher puts each short on a draft release of this repo (a `video.mp4`, then a
`post.json` with the slot time and caption). `.github/workflows/social.yml` calls `social.py`, which posts every
short whose slot has passed to Instagram, TikTok and Threads.

- Post state is kept in `state.enc`, encrypted with the `STATE_KEY` secret, so a rerun only does what is left.
- All keys live in this repo's GitHub secrets; nothing secret is in the code.
- To test without posting, run the workflow by hand with dry run on.
