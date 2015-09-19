This archive contains the data gathered for the following paper:

 * J. Urbano, M. Marrero, D. Martín, J. Morato, K. Robles and J. Lloréns, "[The University Carlos III of Madrid at TREC 2011 Crowdsourcing Track](http://julian-urbano.info/wp-content/uploads/035-university-carlos-iii-madrid-trec-2011-crowdsourcing-track.pdf)", *Text REtrieval Conference*, 2011.

A [single ZIP file](https://github.com/julian-urbano/trec2011-crowdsourcing/archive/master.zip) can be downloaded as well.

## Data

### Files

* `templates/` HIT templates used to crowdsource judgments. Live versions available:
 * [`uc3m.graded`](http://julian-urbano.github.io/trec2011-crowdsourcing/templates/uc3m.graded.html).
 * [`uc3m.slider`](http://julian-urbano.github.io/trec2011-crowdsourcing/templates/uc3m.slider.html).
 * [`uc3m.hterms`](http://julian-urbano.github.io/trec2011-crowdsourcing/templates/uc3m.hterms.html).
* `data/hits.txt` tab-separated file with information about the HITs we submitted to Mechanical Turk.
* `data/workers.txt` tab-separated file with information about all workers that interacted with our server.
* `data/assignments.txt` tab-separated file with information about all interactions with workers, as registered by our server.

### Details

The columns in the data files are:

* `data/hits.txt` (`N` goes from 1 to 5):
 * `set` the corresponding set ID of the five documents shown in the HIT, as in the Track's official data.
 * `topic` the topic number corresponding to the set, as in the Track's official data.
 * `title` our description of the topic.
 * `good` our description of what good documents are for the topic.
 * `bad` our description of what bad documents are for the topic.
 * `docN` the ClueWeb09 document ID of the `N`-th document in the set, as in the Track's official data.
 * `docNkeys1` the first set of five keywords shown to the worker for the `N`-th document.
 * `docNkeys2` the second set of five keywords shown to the worker for the `N`-th document.
 * `docNkeys` which of the two sets of keywords is the correct one for the `N`-th document.
* `data/workers.txt` (`N` goes from 1 to 3):
 * `id` the anonymized worker ID.
 * `country` the country of the worker, as reported by http://www.geobytes.com/IpLocator.htm using the worker's IP address.
 * `runNpre` number of HITs previewed by the worker for the `N`-th run.
 * `runNski` number of HITs skipped or expired (e.g. accepted by the worker but never submitted) for the `N`-th run.
 * `runNacc` number of HITs submitted by the worker and accepted for the `N`-th run.
 * `runNrej` number of HITs submitted by the worker and rejected for the `N`-th run.
* `data/assignments.txt` (`N` goes from 1 to 5):
 * `run` the run for which the interaction was registered (1 to 3).
 * `set` the set ID of the HIT, as in the `hits.txt` file.
 * `worker` the anonymized worker ID, as in the `workers.txt` file.
 * `status` status of the interaction (one of `Preview`, `Skipped`, `Accepted` or `Rejected`).
 * `tsload` timestamp (CET time) of the interaction loading.
 * `tssend` timestamp (CET time) of the interaction end (last timing report for previews, and submission for accepted and rejected HITs).
 * `docNimg` total time (in seconds) the `N-`th document was displayed in the images mode.
 * `docNtxt` total time (in seconds) the `N`-th document was displayed in the text mode.
 * `docNkeys` which of the two sets of keywords was chosen by the worker for the `N`-th document.
 * `docNrel` relevance value give to the `N`-th document: 0 to 2 for run 1, and 0 to 100 for runs 2 and 3.
 * `kfails` number of failures in the keywords questions.
 * `tfails` number of failures in work time.
 * `comment` feedback given by the worker.

Missing values are indicated with the string `NA`.


## License

 * Databases and their contents are distributed under the terms of the [Creative Commons Attribution-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-sa/4.0/).

When using this archive, please cite the above paper:

    @inproceedings{Urbano2011:trec,
      author = {Urbano, Juli\'{a}n and Marrero, M\'{o}nica and Mart\'{\i}n, Diego and Morato, Jorge and Robles, Karina and Llor\'{e}ns, Juan},
      booktitle = {Text REtrieval Conference},
      keywords = {crowdsourcing,relevance judgments,trec,uc3m},
      title = {{The University Carlos III of Madrid at TREC 2011 Crowdsourcing Track}},
      year = {2011}
    }
