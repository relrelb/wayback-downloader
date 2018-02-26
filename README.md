# wayback-downloader
A simple downloader client for the Wayback Machine written in Python.
```
Usage:
	python <script.py> {--help|-h}
	python <script.py> [--matchType {exact|prefix|host|domain}] [--from <timestamp>] [--to <timestamp>] [--limit <snapshots>] [--dry] <url>

Options:
	--help, -h		Display this help message and exit

	--matchType, -m	What results will be downloaded based on <url>
		exact		Download results matching exactly <url>
		prefix		Download results under the path <url>
		host		Download results from host of <url>
		domain		Download results from host of <url> and all subhosts of <url>

	--from, -f		Download results that were captured after this timestamp
	--to, -t		Download results that were captured before this timestamp
		Both <from> and <to> must be a prefix of "yyyyMMddhhmmss"

	--limit, -l		Download at most <snapshots> snapshots

	--dry, -d		List items to be downloaded without downloading them

Example:
	Use the following command:
		python <script.py> --matchType prefix --from 2010 --to 201606 --limit 1000 example.org
	To download at most 1000 abarity pages under example.org between the year of 2010 and the month of June 2016 (inclusive).

For more information, see: https://github.com/internetarchive/wayback/blob/master/wayback-cdx-server/README.md
```
