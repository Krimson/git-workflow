## workflow/repo structure

### » filesystem

- `db` (optional, not recommended to strore db dumps in repos)
- `patches` (optional, hacked someting? Patch it!)
- `www` (drupal root)

### » branches

- `master` (production, stable)
- `DEV` (DEV environment, changes by dev team)
- `ACC` (ACC environment, changes awaiting approval and or testing)
- `ABC-123` (feature branch, local environment. Changes you're working on that aren't quite ready to push to the rest of the team)

### » branching/mergin model examples

- ![master/DEV](http://nvie.com/img/2009/12/bm002.png)
- ![master/DEV/ABC-123](http://www.intellimentsec.com/wp-content/uploads/2012/12/Branches.png)
- master/DEV/ACC
  - ![botanique](http://d.pr/i/BH0L)
  - ![pidpa](http://d.pr/i/7yZl)

