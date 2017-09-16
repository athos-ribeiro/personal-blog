+++
author = "Paul E. Black and Athos Ribeiro."
citation = "March 2016, NIST Internal Report (IR) 8113. DOI 10.6028/NIST.IR.8113 or http://nvlpubs.nist.gov/nistpubs/ir/2016/NIST.IR.8113.pdf. The data and programs to reproduce these results are available at DOI 10.18434/T4WC7V or https://s3.amazonaws.com/nist-ockham-criteria-sate-v-data/ockhamCriteriaSATEVdata.tar.xz (9.3 Megabytes download, 390 Megabytes uncompressed). A README file is available at https://s3.amazonaws.com/nist-ockham-criteria-sate-v-data/README"
date = "2016-05-16T15:07:01-03:00"
file = "NIST.IR.8113.pdf"
title = "SATE V Ockham Sound Analysis Criteria"
type = "published"

+++

Static  analyzers  examine  the  source  or  executable code  of  programs  to  find  problems.  Many  static  analyzers  use  heuristics  or  approximations  to  handle  programs  up  to  millions  of  lines  of  code.  We  established the   Ockham   Sound   Analysis   Criteria   to   recognize static  analyzers  whose  findings  are  always  correct.  In brief  the  criteria  are  (1)  the  analyzer’s  findings  are claimed  to  always  be  correct,  (2)  it  produces  findings for  most  of  a  program,  and  (3)  even  one  incorrect finding  disqualifies  an  analyzer.  This  document  begins by  explaining  the  background  and  requirements  of  the Ockham  Criteria.

In  Static  Analysis  Tool  Exposition  (SATE)  V,  only one  tool  was  submitted  to  be  reviewed.  Pascal  Cuoq and  Florent  Kirchner  ran  the  August  2013  development   version   of   Frama-C   on   pertinent   parts   of the  Juliet  1.2  test  suite.  We  divided  the  warnings into  eight  classes,  including  improper  buffer  access, NULL pointer dereference, integer overflow, and use of uninitialized variable. This document details the many technical  and  theoretical  challenges  we  addressed  to classify  and  review  the  warnings  against  the  Criteria.  It  also  describes  anomalies,  our  observations,  and interpretations.  Frama-C  reports  led  us  to  discover three  unintentional,  systematic  flaws  in  the  Juliet  test suite  involving  416  test  cases.  Our  conclusion  is  that Frama-C satisfied the SATE V Ockham Sound Analysis Criteria.

Certain trade names and company products are mentioned  in  the  text  or  identified.  In  no  case  does  such identification  imply  recommendation  or  endorsement by the National Institute of Standards and Technology (NIST),  nor  does  it  imply  that  the  products  are  necessarily  the  best  available  for  the  purpose. 
