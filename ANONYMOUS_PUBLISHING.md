# Anonymous publishing

Every new checkout must run:

```sh
git config --local user.name 'Anonymous Authors'
git config --local user.email 'iclr-submission7014@users.noreply.github.com'
git config --local core.hooksPath .githooks
chmod +x .githooks/pre-push
```

Authenticate as `iclr-submission7014` only. Before deployment, inspect staged
files for identifying names, emails, institution-specific paths, external links,
and embedded media metadata. Do not merge or cherry-pick identifying history.
The pre-push hook validates every reachable commit's author and committer;
hooks are local safeguards, not server-enforced restrictions.

Verify the public commit metadata and deployment after every push. Freeze the
submission snapshot and record its full commit SHA in the submitted supplement.
