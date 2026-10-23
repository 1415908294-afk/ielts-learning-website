# Public Site content maintenance

The owner requested public access, removal of Oxford A1 entries and randomized study/audio order. Preserve stable IDs and all personal progress records. Active Oxford vocabulary is A2/B1/B2.

GET /api/content is public read-only. All writes to that endpoint are disabled. Never rely on the former private-site boundary for authorization.

For recurring curation, research official IELTS, British Council and IDP preparation/assessment resources and update the source through the Sites skill workflow. Obtain fresh source credentials in the current run; pass only via hidden stdin and never store them in files, prompts or Git. Preserve the project ID and public audience. Run the build and relevant checks, push, package and publish. Verify deployment success. Do not modify user progress or applied database migrations.

Use accurate Chinese meanings, natural collocations and original bilingual examples. Never describe unverified predictions as actual test questions or invent frequency statistics. Keep A1 excluded. Use node build.mjs to update the generated Worker after editing src/index.html. Update the GitHub source snapshot when authorized and available.

Stay quiet without meaningful change. Report unavailable access, failed checks or publication, or required user action. Never report a planned update as complete.
