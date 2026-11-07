# Fixture: fictional project Atlas

All names, dates, and decisions in this fixture are fictional.

## Project history

- January 8: Atlas planned to use PostgreSQL and a weekly Tuesday release.
- January 16: The team selected the name Northstar for its reporting service and assigned ownership to Mira.
- February 2: The team changed releases to Thursdays. Existing deployments remained on PostgreSQL.
- February 13: A proposal to use Redis for the primary database was rejected; Redis was approved for caching only.
- March 1: Northstar ownership moved from Mira to Leo. Mira retained ownership of the import service.
- March 9: A draft proposed storing backups for 30 days. It was never approved.
- March 20: The team approved a 14-day backup retention policy.
- April 4: The public API rate limit was set to 120 requests per minute per API key.
- April 12: The team chose not to set a date for a mobile app release.
- April 27: The public API rate limit changed to 80 requests per minute per API key.
- May 3: Thursday remained the release day, but the release window moved from 10:00 to 15:00 UTC.
- May 12: A plan to migrate to MySQL was discussed but not approved.

## Questions

1. What is Atlas's approved primary database?
2. What day are releases scheduled?
3. Who currently owns Northstar?
4. How long are backups retained?
5. What is the current public API rate limit?
6. What is Redis approved for?
7. What time is the current release window, in UTC?
8. What is the mobile app release date?

## Memory note

Current Atlas decisions: PostgreSQL is the primary database; Redis is used only for caching. Releases are Thursdays at 15:00 UTC. Leo owns Northstar. Backups are retained for 14 days. The public API limit is 80 requests per minute per API key. No mobile app release date has been set.
