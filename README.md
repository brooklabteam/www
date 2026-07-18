# www - lab homepage

### Basics

**www** is a [Jekyll](https://jekyllrb.com/)-generated static site. The published site is built and deployed using [Cloudflare Pages](https://pages.cloudflare.com/), with a domain registered via [Cloudflare](https://www.cloudflare.com).

### Open questions / to confirm

Items surfaced during a content review that need a human decision before they can be fixed:

**Functional errors (the news feed links/sorts wrong):**

- `_posts/2020-03-27-who-what-why-podcast.markdown` — the `date:` (`2019-04-16`) and `link:` (the Journal of Animal Ecology blog) were copy-pasted from the 2019 "disentangling" post. The post is about the **WhoWhatWhy podcast**, so the link points to the wrong site and the wrong date sorts it into 2019 on `/news`. Needs the correct WhoWhatWhy episode URL and intended date.
- `_posts/2020-04-03-the-naked-scientists.markdown` — `date: 2020-05-15` doesn't match the filename date (`2020-04-03`), so it sorts a month off. Confirm which date is correct.

**Details to verify (names/numbers I shouldn't guess at):**

- `publications.md` — author "Mendendall IH" is likely "Mendenhall IH" (Ian Mendenhall).
- `publications.md` — the *Parasites & Vectors* Babesial-infection paper (2019) lists "12 (51): 1307101933"; that page/article field looks corrupted.
- `publications.md` — the 2016 *J. R. Soc. Interface* rubella paper: DOI `10.1098/rsif.2015.110` looks truncated (article `20151101` → likely `10.1098/rsif.2015.1101`), and there's a stray `±` right after the year ("2016±").
