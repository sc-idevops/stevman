# Migrating from Mastodon Accounts

Often times this process encounters issues. At the time of this writing, it's not possible to move your content (i.e. posts) from server to server. However it is possible to push/pull your followers, muted/blocked filters & domains, and your bookmarks. 

## Obtaining Your Data 

It's important that you do this process before your closing server shuts down as they are your source of your data!
1. Access account preferences on the server you are leaving, and choose "Import & Export"
2. Select Data Export and click "Request your Archive". 
3. While that is generated for your posts, you also need to manually download your Follows, Lists, bookmarks, etc which happens instantly vs waiting for your full archive. Just click the little download icon next to each one.
   - Put all of these files into a folder, preferably with your other backups. (You *do* have backups of your important files, ...right?)

## Importing Your Data 

1. Log in to your account on the new instance you are joining. Head to account preferences and click "Import and Export" again. 
2. This time we're headed to the import section. As of now, mastodon only seems to accept the following:
   - Following List
   - Blocking List
   - Muting List
   - Domain Blocking List
   - Bookmarks
3. **If your migration failed or otherwise had issues, you can manually upload a list of your followers on this screen.** You can repeat this process for anything else in the above list.

Note: it asks if you want to *merge* or *overwrite* your existing information. This shouldn't matter too much with a new account but if you are merging several existing accounts into one, it will make a big difference!

## Important Notes

- Downloading just "Your Data Archive" is insufficient! You need to get your follower lists yourself. This seems counter-intuitive enough to merit mentioning here. 