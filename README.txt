===========
tcsv2png
===========

NAME
----
tcsv2png - data visualization of csv data with a time column.

SYNPSIS
-------

::

  tcsv2png [Options] CSV_FILE [COL0 [COLi ...]]



DESCRIPTION 
-----------
tcsv2png uses gnuplot to convert a csv file with a time column
format %H:%m:%S into a chart in png format.

It scales the data to show all of the data sets in the same
png chart.

You can select the columns of interest. The tool uses gnuplot
to generate the chart, so you can customize the script to your
need.

CSV_FILE: a csv file with TAB or semicolon fields separator
COL0:     the column indice that contains the time formated H:M:S
COLi:     column indice to plot

Note that column indice starts with 0 and that the first line
should contains columns headers.


REQUIRES
--------
tcsv2png requires `gnuplot <http://www.gnuplot.info/>`_.


INSTALLATION
------------
::

   sudo easy_install tcsv2png


EXAMPLES
--------

  You can view some screenshots in the `tcsv2png wiki
  <https://github.com/bdelbosc/tcsv2png/wiki>`_

  tcsv2png data.csv 
          Creates data.png file with all the columns, assuming
          column 0 is the time column.

  tcsv2png -v -c -t "Foo title" -o foo.png  data.csv 0 3 5
          Creates foo.png chart with "Foo title" title, column 0 is
	  the time column, plotting column 3 and 5 using smooth
	  csplines rendering.

  tcsv2png -h
          Gives you the available options.
