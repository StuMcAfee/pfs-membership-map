# Posterior Fossa Society membership map

A world map of the cities where Society members work, with the institutions in each city.
Shows no names, email addresses, or member counts.

## Files
- `index.html`: the map page (public).
- `institutions.js`: the map data (public; generated, do not edit by hand).
- `build_membership_map.py`: rebuilds `institutions.js` from the membership list.
- `institution_lookup.csv`: email domain -> institution, city, coordinates. **Private**: kept out of the
  repository by `.gitignore`, because it lists every member's email domain, including excluded ones.

## Updating
1. Save the new membership list somewhere outside this folder.
2. Run `python build_membership_map.py /path/to/Membership_List.xlsx`.
3. If it reports domains missing from `institution_lookup.csv`, add a row for each (status `include` or
   `exclude`) and run it again. To honor an opt-out, set that institution's row to `exclude`.
4. Commit `institutions.js` on a new branch, push, and merge the pull request, as with the hospital map.
