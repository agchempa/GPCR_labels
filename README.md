# gpcr_labels
Label files for the getcontacts package, derived from GPCRdb
(http://gpcrdb.org). Each file maps [3-letter aa code]:[residue number]
to its corresponding Ballesteros-Weinstein number. In order to use
these label files in getcontacts, be sure to prepend the appropriate
chain id to each line.

chain = 'A'     # replace with chain ID
with open(desired_label_file.tsv, 'r') as r_open:
    with open(getcontacts_label_file.tsv, 'w+') as w_open:
        for line in r_open.readlines():
            w_open.write('%s:%s' % (chain, line))
