Created on: 13-09-2025 12:42, note by Youssef Okeil
Status: #idea
Tags: #BaRead #data_base 
# Database Update
1. removed foreign key in `books` called `id` of type `UUID` that points to `listings.bookId`
2. deleted `bookID` from listings, now all products will be pointing to `id` of size `bigint`
3. Added a new foreign key `books.listingId` that points to --> `listings.id` of type `bigint`.
4. Added a new table `clothing` for clothing products. Has columns `listingid` --> `listings(id)`, `categoryId` --> `clothing_categories(id)` , `demographicid` --> `clothing_demographics(id)`, `attributes` of JSON type
5. Added table `clothing_demographics` for gender, in  my imagination we'll use a drop down menu for gender.
![[Pasted image 20250913131103.png| center]]

> NB: Sort order is for ordering in the drop-down menu, yes seems redundant now with id, but if we want to add toddler or infant we can pick where exactly in the drop-down do we want it to be!

6. Added table `clothing_categories` , also will be used in drop-down menus. This will also be used to pick what other fields we'll show to the user. Ex: If user picks `tops` then we'll show a field of sizes of `XS, S, M....` if s/he chooses `shoes` --> show sizes `43,44, 45, ..`
![[Pasted image 20250913131623.png| center]]

> NB:  --> means references, as in foreign key

### MISSING!
- how will we manage sizes? will we make another table of valid sizes? with `category_id` and `size`?
- we need to normalize all column names to either snake_case or camelCase
-----------------
# References