# Lab Report 3
### Maya Beeri-Feldman

## part 1

1. A failure-inducing input
``` 
  @Test
  public void testReversed2() {
    int[] input1 = new int[]{1, 2, 3};
    assertArrayEquals(new int[]{3, 2, 1}, ArrayExamples.reversed(input1));
  }
```
2. An input that doesn't induce a failure
``` 
@Test
  public void testReversed() {
    int[] input1 = { };
    assertArrayEquals(new int[]{ }, ArrayExamples.reversed(input1));
```
3. The symptom
![image](https://github.com/mbeerifeldman/cse15l-lab-reports/assets/114952150/4d23694e-31cd-45da-9873-c756d55ec25a)

4. Before code
``` 
  static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = newArray[arr.length - i - 1];
    }
    return arr;
  }
```
5. After code
``` 
  static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    newArray = arr.clone();
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = newArray[arr.length - i - 1];
    }
    return arr;
  }
```
The issue was that `arr` was being filled with values of `newArray` but that is an empty array that was only just initialized, meaning 
`arr` is not being filled with anything but zeros. Fixing it meant filling `newArray` first with the original array by making a copy and then 
filling in the original with the reversed order of `newArray`.

## part 2
1.
```
Bluestarr@MacBook-Pro-8 docsearch % grep -h  "biology"  technical/biomed/*.txt
        in silico biology. It is clear that
          is reflected in the better understanding of their biology
        biology community as the Myers/Miller algorithm [ 31 ] .
          sample biology (Table 2). The most consistent cluster
          match the sample biology (Figure 2A) and for 16 of these
          biology in the pilot data set. The sample dendrogram
          profiles and the pathobiology of the RCCa tumor
        sets. The pattern was consistent with the biology of the
        surprising, but entirely consistent with the biology of
        is a fundamental problem in biology. We have designed new
        molecular biology and genetics.
        recent study in systems biology elegantly demonstrates [ 1
        understanding of yeast biology, where homogeneous cultures
        including biology [ 6 7 8 9 10 ] . However, calculation of
        approaches to studying the biology of cytokinesis.
        introduced to the cell biology community as a millimolar
        cell biology community because of its rapid and reversible
          Standard molecular biology methods were used in making
        cell biology of the relevant cells.
        example of TED's adaptation to baculovirus biology is the
        research subjects in evolutionary biology since T. H.
        of publications [ 1 2 ] spanning the biology, moral
        physiology, neurobiology, paleontology, and astrobiology.
        biology of animal development.
        that requires less RNA. Several molecular biology
        biology approaches such as northern blotting, western
          Chemicals and reagents were molecular biology grade or
        of the manuscript regarding the biology of avulsion
        Computational biology strives to extract the maximum
          Inflammation, Metabolism, Neurobiology, Toxicology, and
        envelope biology.
        advancing the fields of biology and medicine. Most
        research in reproductive biology. For example, the study of
          dissolved in 25 μl of molecular biology grade formamide.
          http://opal.biology.gatech.edu/GeneMark/eukhmm.cgi?org=H.sapiens.
        http://microbiology.okstate.edu/faculty/burnap/index.html.
          transduction on T cell biology, and to examine the
        studies of lymphocyte biology. In an effort to facilitate
          Alabama at Birmingham Department of Microbiology
        endocytic tracer molecules. These cell biology studies
          Microbiology) and 0.05% Tween 80 and ferric mycobactin J
        from the Viking biology mission to Mars. In the Viking's
        Viking biology experiments [ 20 ] . A molecule such as DCIP
        the function of this gene family in the biology of 
        biology of 
        Microbiology Meeting, Salt Lake City, May 2002
        model do not always reflect the biology of RNA viruses. In
        biology might indeed have been responsible for the observed
        Viking biology experiments. Goldfield, et al. [ 5 ] further
        original biology experiments aboard Viking, though the
          General molecular biology
          Bacterial media and molecular biology techniques were as
          biology reagents (except as noted) were from Sigma (St.
          chronobiology is the " chi-squared periodogram" [ 41 42 ]
        reasons. First, it is likely that insights into the biology
        biology study, in situ hybridization studies. J. Xu carried
        exploration of genetic influence on human biology. However,
        and bitter ligands for genetic and molecular biology
          alter the biology of these genes, the 3' UTR insertion in
        physiology and pathobiology. These include urokinase-type
        . In evolutionary biology, the possibility that HLA
        of what IL-6 does in other model systems of cancer biology.
        With breakthroughs in molecular biology, basic
        has been studied extensively by the radiobiology community.
        expanded to include treatment delivery, tissue biology, and
        insurance and biology [ 2 3 4 5 6 7 8 ] . The educational
        multi-factorial biology-utilization model. [ 9 ]
        biology. Several inducible systems have been developed to
        therapy and tumor biology studies in mature animals.
        when inoculated orthotopically it reproduces the biology of
        biology and biotechnology applications. Most recently, the
        molecular biology enzymes. For example, a compartmentalized
        adapted to a range of molecular biology enzymes that act on
        exploited in a variety of technologies in molecular biology
          Microbiology Workstation Bioscreen C (Labsystems, Inc.,
        of molecular biology [ 1 ] . A recent adaptation of this
        important in dissecting Fhit cell biology and regulating
        of how scaling impacts the biology of the mosquitoes,
        MTX-induced cascade in normal cellular biology remains
          organism's biology. Even though structure prediction
        mechanisms of the body, the biology of disease, and the
        importance in biology. The PP1 and PP2A phosphatases are
            min) and diluted to 400 μl in molecular biology grade
        tissues have been used to characterize the biology of the
        biology of certain cancers, in particular basal cell
        JRS provided cell biology expertise concerning the
          biology of fission yeast facilitates the identification
        aseptically to the clinical microbiology laboratory where
        microbiology laboratory to perform and the most frequently
        A number of investigators have examined the microbiology
        least expensive tests for a clinical microbiology
        investigate the biology and genetics of GC transformation,
        of epigenetic changes in GCT etiology and biology are not
        biology.
        about the physiology and biology of ovarian SC, they have
          have an influence on the biology of certain tumors [ 14,
          length appears to have an influence on the biology of
        biology, and MMP gene regulation, this microarray
        roles in chondrocyte biology are yet to be defined. While
          understanding of this biology has been derived from the
          biology improves, investigators have also proposed that
        cells and NK cells whose role in bone biology is only
        of Clinical Microbiology and Infectious Diseases (28-31 May
        sequence-structure patterns and is rooted in the biology of
        other areas of biology [ 4]. Two-dimensional gels have been
        biology. A variety of representations are used in print or
          descriptive language for biology can offer additional
          'complete'? For a domain such as biology which is almost
          modeling in biology (for example Stella™ [ 26], SAAM II™
          such difficulties, biology, perhaps more than other
        technical disciplines. The major challenge is that biology
        implementation of a graphic language for biology is not
        insights to both L1 biology and the mechanisms by which L1s
          involved in the biology of interferons.
        because our knowledge of biology is constantly changing,
        and because biology itself is often unconstrained by rules
        schema. In any genome, normal biology conspires to break
        the experimentally known biology of the organism.
        are expected to share more aspects of their biology in
        active areas of research in computational biology [ 6],
          subspaces remains a goal in biology. Another example is
          An important question in biology is how many different
        insight into many areas of cell biology, and statistical
        these modules has thrown considerable light on the biology
        In regard to genomic biology, Mantegna 
        genomic biology include the occurrence of protein families
        throughout genomic biology. As noted above, previous
        laws in biology and discuss several models that aim to
          outside biology [ 29, 30, 31, 32]. Previous publications
          genomic biology have linked such stochastic dynamical
          biology of Toll-like receptors, the NFκB-dominated
        biology that is occurring in a particular dataset, making
        specific areas of biology that warrant more detailed
        gene-expression changes across all biology. On a practical
        known biology [ 3]. Several other pathway programs such as
        identifying those areas of biology showing correlated
        rapidly identifying those areas of biology that warrant
        developmental biology has produced a wealth of genetic and
        understanding of root-knot nematode biology and applied
          nematodes have adapted a portion of Nod factor biology to
        Meloidogyne molecular biology include
        revolutionizing biology. That much is universally agreed.
          the biology of CCl 
        GenBank. Genes found to be associated with the biology of
          biology.
        investigations into the molecular biology of cancers are
        global systems level, the biology behind the differences in
        revolutionized molecular biology. The sequencing of entire
        tools able to interrogate biology on a genome-wide scale
          (Becton-Dickinson Microbiology, Cockeysville, MD).
```
2.  
```
Bluestarr@MacBook-Pro-8 docsearch % grep -h  "microscopically"  technical/biomed/*.txt
          terms. Microvilli are light microscopically distinct from
          diameter microscopically, and mean cell size was
          microscopically, lysed, and levels of AppppN and ApppN
        microscopically have been suggested to be due to
        microscopically. We observed the tail and behavioral
          larvae were microscopically examined at 100× to verify
          sections were analyzed microscopically. The 
          samples also showed microscopically normal regions with
          microscopically, centrifuged at 800 rpm for 10 min at
          microscopically for complete break of the nuclei. The
          macroscopically and microscopically normal. The cells
```
The command being used here is `grep -h` which will print out the lines that match the string given but without any of the file names/origin. 
3. 
```
Bluestarr@MacBook-Pro-8 docsearch % grep -c  "microscopically"  technical/biomed/*.txt
technical/biomed/1468-6708-3-1.txt:0
technical/biomed/1468-6708-3-10.txt:0
technical/biomed/1468-6708-3-3.txt:0
technical/biomed/1468-6708-3-4.txt:0
technical/biomed/1468-6708-3-7.txt:0
technical/biomed/1471-2091-2-10.txt:0
technical/biomed/1471-2091-2-11.txt:0
technical/biomed/1471-2091-2-12.txt:0
technical/biomed/1471-2091-2-13.txt:0
technical/biomed/1471-2091-2-16.txt:0
technical/biomed/1471-2091-2-5.txt:0
technical/biomed/1471-2326-2-4.txt:0
technical/biomed/1471-2334-1-10.txt:1
technical/biomed/1471-2334-1-13.txt:0
technical/biomed/1471-2334-1-17.txt:0
technical/biomed/1471-2334-1-21.txt:0
technical/biomed/1471-2334-1-24.txt:0
technical/biomed/1471-2334-1-9.txt:0
technical/biomed/1471-2334-2-1.txt:0
technical/biomed/1471-2334-2-24.txt:0
technical/biomed/1471-2334-2-26.txt:0
technical/biomed/1471-2334-2-27.txt:0
technical/biomed/1471-2334-2-29.txt:0
technical/biomed/1471-2334-2-5.txt:0
technical/biomed/1471-2334-2-6.txt:0
technical/biomed/1471-2334-2-7.txt:0
technical/biomed/1471-2334-3-10.txt:0
technical/biomed/1471-2334-3-11.txt:0
technical/biomed/1471-2334-3-12.txt:0
technical/biomed/1471-2334-3-13.txt:0
technical/biomed/1471-2334-3-15.txt:0
technical/biomed/1471-2334-3-9.txt:0
technical/biomed/1471-2350-2-11.txt:0
technical/biomed/1471-2350-2-12.txt:0
technical/biomed/1471-2350-2-2.txt:0
technical/biomed/1471-2350-2-8.txt:0
technical/biomed/1471-2350-3-1.txt:0
technical/biomed/1471-2350-3-12.txt:0
technical/biomed/1471-2350-3-7.txt:0
technical/biomed/1471-2350-3-9.txt:0
technical/biomed/1471-2350-4-2.txt:0
technical/biomed/1471-2350-4-3.txt:0
technical/biomed/1471-2350-4-4.txt:0
technical/biomed/1471-2350-4-6.txt:0
technical/biomed/1471-2369-3-1.txt:0
technical/biomed/1471-2369-3-10.txt:0
technical/biomed/1471-2369-3-6.txt:0
technical/biomed/1471-2369-3-9.txt:0
technical/biomed/1471-2369-4-1.txt:0
technical/biomed/1471-2369-4-5.txt:0
technical/biomed/1471-2377-1-2.txt:0
technical/biomed/1471-2377-2-4.txt:0
technical/biomed/1471-2377-2-6.txt:0
technical/biomed/1471-2377-3-4.txt:0
technical/biomed/1471-2407-1-13.txt:0
technical/biomed/1471-2407-1-15.txt:0
technical/biomed/1471-2407-1-19.txt:0
technical/biomed/1471-2407-1-6.txt:0
technical/biomed/1471-2407-2-11.txt:0
technical/biomed/1471-2407-2-12.txt:0
technical/biomed/1471-2407-2-15.txt:0
technical/biomed/1471-2407-2-16.txt:0
technical/biomed/1471-2407-2-17.txt:0
technical/biomed/1471-2407-2-18.txt:0
technical/biomed/1471-2407-2-19.txt:0
technical/biomed/1471-2407-2-22.txt:0
technical/biomed/1471-2407-2-23.txt:0
technical/biomed/1471-2407-2-3.txt:0
technical/biomed/1471-2407-2-31.txt:0
technical/biomed/1471-2407-2-33.txt:1
technical/biomed/1471-2407-2-8.txt:0
technical/biomed/1471-2407-2-9.txt:0
technical/biomed/1471-2407-3-14.txt:0
technical/biomed/1471-2407-3-15.txt:0
technical/biomed/1471-2407-3-16.txt:0
technical/biomed/1471-2407-3-18.txt:0
technical/biomed/1471-2407-3-3.txt:0
technical/biomed/1471-2407-3-4.txt:0
technical/biomed/1471-2407-3-5.txt:0
technical/biomed/1471-2415-3-1.txt:0
technical/biomed/1471-2415-3-3.txt:0
technical/biomed/1471-2415-3-4.txt:0
technical/biomed/1471-2415-3-5.txt:0
technical/biomed/1471-2431-2-1.txt:0
technical/biomed/1471-2431-2-11.txt:0
technical/biomed/1471-2431-2-12.txt:0
technical/biomed/1471-2431-2-4.txt:0
technical/biomed/1471-2431-3-3.txt:0
technical/biomed/1471-2431-3-4.txt:0
technical/biomed/1471-2431-3-5.txt:0
technical/biomed/1471-2431-3-6.txt:0
technical/biomed/1471-244X-2-9.txt:0
technical/biomed/1471-244X-3-5.txt:0
technical/biomed/1471-2458-1-9.txt:0
technical/biomed/1471-2458-2-11.txt:0
technical/biomed/1471-2458-2-16.txt:0
technical/biomed/1471-2458-2-18.txt:0
technical/biomed/1471-2458-2-21.txt:0
technical/biomed/1471-2458-2-25.txt:0
technical/biomed/1471-2458-2-3.txt:0
technical/biomed/1471-2458-2-6.txt:0
technical/biomed/1471-2458-3-11.txt:0
technical/biomed/1471-2458-3-2.txt:0
technical/biomed/1471-2458-3-20.txt:0
technical/biomed/1471-2458-3-5.txt:0
technical/biomed/1471-2458-3-9.txt:0
technical/biomed/1471-2466-1-1.txt:0
technical/biomed/1471-2466-2-3.txt:0
technical/biomed/1471-2466-2-4.txt:0
technical/biomed/1471-2466-3-1.txt:0
technical/biomed/1471-2474-2-1.txt:0
technical/biomed/1471-2474-2-2.txt:0
technical/biomed/1471-2474-2-3.txt:0
technical/biomed/1471-2474-3-23.txt:0
technical/biomed/1471-2474-3-3.txt:0
technical/biomed/1471-2474-4-4.txt:0
technical/biomed/1471-2474-4-8.txt:0
technical/biomed/1471-2490-3-2.txt:0
technical/biomed/1471-5945-1-3.txt:0
technical/biomed/1471-5945-2-13.txt:0
technical/biomed/1471-5945-3-3.txt:0
technical/biomed/1472-6750-1-11.txt:0
technical/biomed/1472-6750-1-12.txt:0
technical/biomed/1472-6750-1-13.txt:0
technical/biomed/1472-6750-1-6.txt:0
technical/biomed/1472-6750-1-8.txt:0
technical/biomed/1472-6750-2-10.txt:0
technical/biomed/1472-6750-2-13.txt:0
technical/biomed/1472-6750-2-14.txt:0
technical/biomed/1472-6750-2-2.txt:0
technical/biomed/1472-6750-2-21.txt:0
technical/biomed/1472-6750-3-11.txt:0
technical/biomed/1472-6750-3-4.txt:0
technical/biomed/1472-6750-3-6.txt:0
technical/biomed/1472-6769-1-1.txt:0
technical/biomed/1472-6769-1-2.txt:0
technical/biomed/1472-6769-1-3.txt:0
technical/biomed/1472-6769-1-4.txt:0
technical/biomed/1472-6785-1-3.txt:0
technical/biomed/1472-6785-1-5.txt:0
technical/biomed/1472-6785-2-6.txt:0
technical/biomed/1472-6785-2-7.txt:0
technical/biomed/1472-6793-1-11.txt:0
technical/biomed/1472-6793-1-12.txt:0
technical/biomed/1472-6793-1-15.txt:0
technical/biomed/1472-6793-1-2.txt:0
technical/biomed/1472-6793-1-6.txt:0
technical/biomed/1472-6793-1-8.txt:0
technical/biomed/1472-6793-2-1.txt:0
technical/biomed/1472-6793-2-11.txt:0
technical/biomed/1472-6793-2-16.txt:0
technical/biomed/1472-6793-2-17.txt:0
technical/biomed/1472-6793-2-18.txt:0
technical/biomed/1472-6793-2-19.txt:0
technical/biomed/1472-6793-2-2.txt:0
technical/biomed/1472-6793-2-4.txt:0
technical/biomed/1472-6793-2-5.txt:0
technical/biomed/1472-6793-2-8.txt:0
technical/biomed/1472-6793-3-3.txt:0
technical/biomed/1472-6793-3-4.txt:0
technical/biomed/1472-6793-3-5.txt:0
technical/biomed/1472-6793-3-6.txt:0
technical/biomed/1472-6807-1-1.txt:0
technical/biomed/1472-6807-2-1.txt:0
technical/biomed/1472-6807-2-2.txt:0
technical/biomed/1472-6807-2-3.txt:0
technical/biomed/1472-6807-2-4.txt:0
technical/biomed/1472-6807-2-5.txt:0
technical/biomed/1472-6807-2-9.txt:0
technical/biomed/1472-6807-3-1.txt:0
technical/biomed/1472-6807-3-2.txt:0
technical/biomed/1472-6815-2-3.txt:0
technical/biomed/1472-6823-2-2.txt:0
technical/biomed/1472-6823-3-1.txt:0
technical/biomed/1472-6831-2-2.txt:0
technical/biomed/1472-6831-3-1.txt:0
technical/biomed/1472-684X-1-5.txt:0
technical/biomed/1472-684X-2-1.txt:0
technical/biomed/1472-684X-2-2.txt:0
technical/biomed/1472-6874-2-1.txt:0
technical/biomed/1472-6874-2-13.txt:0
technical/biomed/1472-6874-2-8.txt:0
technical/biomed/1472-6874-3-2.txt:0
technical/biomed/1472-6882-1-10.txt:0
technical/biomed/1472-6882-1-11.txt:0
technical/biomed/1472-6882-1-12.txt:0
technical/biomed/1472-6882-1-7.txt:0
technical/biomed/1472-6882-2-10.txt:0
technical/biomed/1472-6882-2-5.txt:0
technical/biomed/1472-6882-3-1.txt:0
technical/biomed/1472-6882-3-3.txt:0
technical/biomed/1472-6890-1-4.txt:0
technical/biomed/1472-6890-2-5.txt:0
technical/biomed/1472-6890-3-2.txt:0
technical/biomed/1472-6904-1-2.txt:0
technical/biomed/1472-6904-2-4.txt:0
technical/biomed/1472-6904-2-5.txt:0
technical/biomed/1472-6904-2-7.txt:0
technical/biomed/1472-6904-3-1.txt:0
technical/biomed/1472-6920-1-3.txt:0
technical/biomed/1472-6920-2-1.txt:0
technical/biomed/1472-6920-2-3.txt:0
technical/biomed/1472-6947-1-2.txt:0
technical/biomed/1472-6947-1-5.txt:0
technical/biomed/1472-6947-1-6.txt:0
technical/biomed/1472-6947-2-4.txt:0
technical/biomed/1472-6947-2-7.txt:0
technical/biomed/1472-6947-3-5.txt:0
technical/biomed/1472-6947-3-8.txt:0
technical/biomed/1472-6955-2-1.txt:0
technical/biomed/1472-6963-1-11.txt:0
technical/biomed/1472-6963-1-8.txt:0
technical/biomed/1472-6963-2-10.txt:0
technical/biomed/1472-6963-3-1.txt:0
technical/biomed/1472-6963-3-11.txt:0
technical/biomed/1472-6963-3-12.txt:0
technical/biomed/1472-6963-3-13.txt:0
technical/biomed/1472-6963-3-14.txt:0
technical/biomed/1472-6963-3-6.txt:0
technical/biomed/1472-6963-3-7.txt:0
technical/biomed/1475-2832-1-1.txt:0
technical/biomed/1475-2867-2-10.txt:0
technical/biomed/1475-2867-2-15.txt:0
technical/biomed/1475-2867-2-7.txt:0
technical/biomed/1475-2867-3-12.txt:0
technical/biomed/1475-2867-3-2.txt:0
technical/biomed/1475-2867-3-3.txt:0
technical/biomed/1475-2867-3-4.txt:0
technical/biomed/1475-2875-1-14.txt:0
technical/biomed/1475-2875-1-5.txt:0
technical/biomed/1475-2875-2-10.txt:0
technical/biomed/1475-2875-2-14.txt:0
technical/biomed/1475-2875-2-4.txt:0
technical/biomed/1475-2883-2-11.txt:1
technical/biomed/1475-2891-1-2.txt:0
technical/biomed/1475-2891-2-1.txt:0
technical/biomed/1475-4924-1-10.txt:0
technical/biomed/1475-4924-1-5.txt:0
technical/biomed/1475-925X-2-1.txt:0
technical/biomed/1475-925X-2-10.txt:0
technical/biomed/1475-925X-2-11.txt:0
technical/biomed/1475-925X-2-12.txt:0
technical/biomed/1475-925X-2-3.txt:0
technical/biomed/1475-925X-2-6.txt:0
technical/biomed/1475-9268-1-1.txt:0
technical/biomed/1475-9268-1-2.txt:0
technical/biomed/1475-9276-1-3.txt:0
technical/biomed/1476-069X-1-3.txt:0
technical/biomed/1476-069X-2-2.txt:0
technical/biomed/1476-069X-2-4.txt:0
technical/biomed/1476-069X-2-7.txt:0
technical/biomed/1476-069X-2-9.txt:0
technical/biomed/1476-0711-2-3.txt:0
technical/biomed/1476-0711-2-7.txt:0
technical/biomed/1476-072X-2-3.txt:0
technical/biomed/1476-072X-2-4.txt:0
technical/biomed/1476-4598-1-3.txt:0
technical/biomed/1476-4598-1-5.txt:0
technical/biomed/1476-4598-1-6.txt:0
technical/biomed/1476-4598-1-8.txt:0
technical/biomed/1476-4598-2-1.txt:0
technical/biomed/1476-4598-2-2.txt:0
technical/biomed/1476-4598-2-20.txt:0
technical/biomed/1476-4598-2-22.txt:0
technical/biomed/1476-4598-2-24.txt:0
technical/biomed/1476-4598-2-25.txt:0
technical/biomed/1476-4598-2-28.txt:0
technical/biomed/1476-4598-2-3.txt:0
technical/biomed/1476-511X-1-2.txt:0
technical/biomed/1476-511X-2-2.txt:0
technical/biomed/1476-511X-2-3.txt:0
technical/biomed/1476-5918-1-2.txt:0
technical/biomed/1476-9433-1-2.txt:0
technical/biomed/1476-9433-1-3.txt:0
technical/biomed/1477-5956-1-1.txt:0
technical/biomed/1477-7525-1-10.txt:0
technical/biomed/1477-7525-1-12.txt:0
technical/biomed/1477-7525-1-9.txt:0
technical/biomed/1477-7819-1-10.txt:0
technical/biomed/1477-7827-1-13.txt:0
technical/biomed/1477-7827-1-17.txt:0
technical/biomed/1477-7827-1-21.txt:0
technical/biomed/1477-7827-1-23.txt:0
technical/biomed/1477-7827-1-27.txt:0
technical/biomed/1477-7827-1-31.txt:0
technical/biomed/1477-7827-1-36.txt:0
technical/biomed/1477-7827-1-43.txt:0
technical/biomed/1477-7827-1-46.txt:0
technical/biomed/1477-7827-1-48.txt:0
technical/biomed/1477-7827-1-54.txt:0
technical/biomed/1477-7827-1-6.txt:0
technical/biomed/1477-7827-1-9.txt:1
technical/biomed/rr166.txt:1
technical/biomed/rr167.txt:0
technical/biomed/rr171.txt:0
technical/biomed/rr172.txt:0
technical/biomed/rr191.txt:0
technical/biomed/rr196.txt:0
technical/biomed/rr37.txt:0
technical/biomed/rr73.txt:0
technical/biomed/rr74.txt:0
```
4. 
```
Bluestarr@MacBook-Pro-8 docsearch % grep -c  "cell"  technical/biomed/*.txt
technical/biomed/1468-6708-3-1.txt:4
technical/biomed/1468-6708-3-10.txt:0
technical/biomed/1468-6708-3-3.txt:1
technical/biomed/1468-6708-3-4.txt:0
technical/biomed/1468-6708-3-7.txt:3
technical/biomed/1471-2091-2-10.txt:58
technical/biomed/1471-2091-2-11.txt:153
technical/biomed/1471-2091-2-12.txt:3
technical/biomed/1471-2091-2-13.txt:3
technical/biomed/1471-2091-2-16.txt:1
technical/biomed/1471-2091-2-5.txt:180
technical/biomed/1471-2091-2-7.txt:17
technical/biomed/1471-2091-2-9.txt:4
technical/biomed/1471-2091-3-13.txt:2
technical/biomed/1471-2091-3-14.txt:150
technical/biomed/1471-2091-3-15.txt:22
technical/biomed/1471-2091-3-16.txt:17
technical/biomed/1471-2091-3-17.txt:0
technical/biomed/1471-2091-3-18.txt:1
technical/biomed/1471-2091-3-22.txt:32
technical/biomed/1471-2091-3-23.txt:18
technical/biomed/1471-2091-3-30.txt:77
technical/biomed/1471-2091-3-31.txt:22
technical/biomed/1471-2091-3-4.txt:7
technical/biomed/1471-2091-3-8.txt:78
technical/biomed/1471-2091-4-1.txt:80
technical/biomed/1471-2091-4-5.txt:6
technical/biomed/1471-2105-1-1.txt:21
technical/biomed/1471-2105-2-1.txt:22
technical/biomed/1471-2105-2-8.txt:1
technical/biomed/1471-2105-2-9.txt:0
technical/biomed/1471-2105-3-12.txt:0
technical/biomed/1471-2105-3-14.txt:1
technical/biomed/1471-2105-3-16.txt:9
technical/biomed/1471-2105-3-17.txt:1
technical/biomed/1471-2105-3-18.txt:11
technical/biomed/1471-2105-3-2.txt:36
technical/biomed/1471-2105-3-22.txt:9
technical/biomed/1471-2105-3-23.txt:0
technical/biomed/1471-2105-3-24.txt:0
technical/biomed/1471-2105-3-26.txt:30
technical/biomed/1471-2105-3-28.txt:0
technical/biomed/1471-2105-3-3.txt:12
technical/biomed/1471-2105-3-30.txt:1
technical/biomed/1471-2105-3-34.txt:32
technical/biomed/1471-2105-3-37.txt:3
technical/biomed/1471-2105-3-38.txt:4
technical/biomed/1471-2105-3-4.txt:5
technical/biomed/1471-2105-3-6.txt:0
technical/biomed/1471-2105-4-13.txt:9
technical/biomed/1471-2105-4-24.txt:2
technical/biomed/1471-2105-4-25.txt:1
technical/biomed/1471-2105-4-26.txt:1
technical/biomed/1471-2105-4-27.txt:2
technical/biomed/1471-2105-4-28.txt:1
technical/biomed/1471-2105-4-31.txt:0
technical/biomed/1471-2121-1-2.txt:10
technical/biomed/1471-2121-2-1.txt:77
technical/biomed/1471-2121-2-10.txt:143
technical/biomed/1471-2121-2-11.txt:109
technical/biomed/1471-2121-2-12.txt:35
technical/biomed/1471-2121-2-15.txt:107
technical/biomed/1471-2121-2-18.txt:130
technical/biomed/1471-2121-2-21.txt:60
technical/biomed/1471-2121-2-22.txt:1
technical/biomed/gb-2003-4-4-r26.txt:22
technical/biomed/gb-2003-4-4-r28.txt:4
technical/biomed/gb-2003-4-5-r30.txt:2
technical/biomed/gb-2003-4-5-r32.txt:17
technical/biomed/gb-2003-4-5-r34.txt:1
technical/biomed/gb-2003-4-6-r37.txt:54
technical/biomed/gb-2003-4-6-r39.txt:11
technical/biomed/gb-2003-4-6-r41.txt:0
technical/biomed/gb-2003-4-7-r42.txt:2
technical/biomed/gb-2003-4-7-r43.txt:5
technical/biomed/gb-2003-4-7-r46.txt:110
technical/biomed/gb-2003-4-8-r50.txt:2
technical/biomed/gb-2003-4-8-r51.txt:2
technical/biomed/gb-2003-4-9-r57.txt:4
technical/biomed/gb-2003-4-9-r58.txt:1
technical/biomed/gb-2003-4-9-r60.txt:6
technical/biomed/rr166.txt:34
technical/biomed/rr167.txt:16
technical/biomed/rr171.txt:52
technical/biomed/rr172.txt:64
technical/biomed/rr191.txt:58
technical/biomed/rr196.txt:0
technical/biomed/rr37.txt:0
technical/biomed/rr73.txt:14
technical/biomed/rr74.txt:2
```
The command `grep -c` will list out every file and the number of times the inputted string appears for each file. (I apologize but in order to shorten this pdf from 45 pages I removed some of the output which was just more files dispalying the same behavior of listing the amount of times string was present in the file.)

5. 
```
Bluestarr@MacBook-Pro-8 docsearch % grep -w  "cell culture"  technical/biomed/*.txt
technical/biomed/1471-2091-2-5.txt:          5were seeded in quadruplicate into Falcon cell culture
technical/biomed/1471-2091-3-23.txt:        study. NM participated in insect cell culture and helped in
technical/biomed/1471-2121-2-18.txt:        matrix assembly in cell culture and in vivo, and to
technical/biomed/1471-2121-3-10.txt:          10 5per 100 mm cell culture dish with DMEM containing 5%
technical/biomed/1471-2121-3-11.txt:          unstimulated cell culture, but this was not enhanced by
technical/biomed/1471-2121-3-11.txt:          3B,3C). The cell culture was still confluent (Fig. 2B)
technical/biomed/1471-2121-3-11.txt:          investigate whether maturation of the cell culture
technical/biomed/1471-2121-3-11.txt:        that cell culture maturation increased resistance to
technical/biomed/1471-2121-3-11.txt:          Endothelial cell culture
technical/biomed/1471-2121-3-11.txt:          supernatant from cell culture was harvested and annexin
technical/biomed/1471-2121-3-11.txt:          medium. After treatment the cell culture supernatant was
technical/biomed/1471-2121-3-11.txt:          One hundred μL of medium or cell culture supernatant
technical/biomed/1471-2121-3-4.txt:          DNA manipulation and cell culture
technical/biomed/1471-2121-3-6.txt:          have been observed in a variety of cell culture models [
technical/biomed/1471-213X-2-8.txt:        Wnt proteins can be used as reagents in cell culture,
technical/biomed/1471-213X-3-2.txt:        murine IL-3 in mouse bone marrow cell culture [ 23 24 ] .
technical/biomed/1471-213X-3-4.txt:        is also remarkable, as apparent from our cell culture
technical/biomed/1471-213X-3-4.txt:        these possibilities, we sought to employ cell culture
technical/biomed/1471-2148-1-1.txt:        infection between cells within insects or in cell culture.
technical/biomed/1471-2156-3-17.txt:          600 cell culture was washed into YP
technical/biomed/1471-2156-4-5.txt:        cell culture media [ 17 ] and aqueous humor [ 12 ] . The
technical/biomed/1471-2156-4-5.txt:        manuscript. NJ carried out the cell culture, transfections
technical/biomed/1471-2172-2-9.txt:          Neutrophil isolation and cell culture
technical/biomed/1471-2172-3-16.txt:          exponential population growth in cell culture (Figure
technical/biomed/1471-2172-3-16.txt:          cell culture [ 60 ] . BCL 
technical/biomed/1471-2172-3-2.txt:        our cell culture assay. Our criterion for an epitope was an
technical/biomed/1471-2172-3-9.txt:          cell culture, DBT, Govt., of India, Pune, India. rIL-2
technical/biomed/1471-2180-1-28.txt:        periods of time in cell culture without selection
technical/biomed/1471-2180-1-34.txt:        infection in cell culture. Using two different RSV gene
technical/biomed/1471-2180-1-34.txt:        application in cell culture only requires the standard
technical/biomed/1471-2180-1-8.txt:          6 confluent HEL cell culture flasks was then removed. Two
technical/biomed/1471-2180-2-26.txt:          Podocyte cell culture and infection
technical/biomed/1471-2180-3-5.txt:          Transwell ®cell culture chamber inserts. The inserts were
technical/biomed/1471-2180-3-5.txt:          Normal mouse osteoblast cell culture
technical/biomed/1471-2180-3-5.txt:          or 250:1 was added separately to Transwell ®cell culture
technical/biomed/1471-2180-3-5.txt:        purified bacterial products and cell culture inserts, and
technical/biomed/1471-2180-3-9.txt:          mRNA in mammalian cell culture [ 24 ] , and our
technical/biomed/1471-2180-3-9.txt:          hrs of cell culture.
technical/biomed/1471-2180-3-9.txt:        In cell culture, a peptide of this sequence inhibited
technical/biomed/1471-2199-2-4.txt:          F9 and C2C12 cell culture and
technical/biomed/1471-2199-3-11.txt:        attachment to the surface of a cell culture dish [ 25 26 ]
technical/biomed/1471-2199-3-11.txt:        from attachment to the matrix of the cell culture dish [ 37
technical/biomed/1471-2199-3-7.txt:        polyphosphates were submicromolar in every cell culture
technical/biomed/1471-2199-4-4.txt:          medium of Ad5 Adapt mhAB infected CHO cell culture in
technical/biomed/1471-2202-2-2.txt:        manipulation in a rigorously defined cell culture system.
technical/biomed/1471-2210-1-7.txt:          LPS-free 75-and 162-cm 2vented cell culture flasks,
technical/biomed/1471-2210-1-7.txt:          polystyrene cell culture dishes (60 × 15 mm) were
technical/biomed/1471-2210-1-7.txt:          75- or 162-cm 2vented cell culture flasks with DMEM
technical/biomed/1471-2210-1-7.txt:          mm polystyrene cell culture dishes, 96-well cell culture
technical/biomed/1471-2210-1-7.txt:          clusters, or 24-well cell culture clusters, with DMEM
technical/biomed/1471-2210-1-7.txt:          plated in LPS-free 96-well cell culture clusters 24 hours
technical/biomed/1471-2210-1-7.txt:          polystyrene cell culture dish) were treated with (1) 1 mM
technical/biomed/1471-2210-1-7.txt:          (250,000 cells/ 24-well cell culture clusters) were
technical/biomed/1471-2210-1-8.txt:          Aortic smooth muscle cell culture
technical/biomed/1471-2210-2-9.txt:        Desensitization occurs both in cell culture systems [ 10 11
technical/biomed/1471-2210-2-9.txt:        response to agonist treatment in transfected cell culture
technical/biomed/1471-2334-1-24.txt:        essential for virus replication in cell culture [ 7 ] ,
technical/biomed/1471-2334-2-7.txt:          MO). For cell culture assays, 10 mg/ml stock solutions
technical/biomed/1471-2334-3-9.txt:        in cell culture.
technical/biomed/1471-2350-3-12.txt:        JT carried out the cell culture, single cell cloning,
technical/biomed/1471-2369-3-6.txt:        previous studies, within the limits of the cell culture
technical/biomed/1471-2369-3-6.txt:        maintained cell culture and was involved in experimental
technical/biomed/1471-2369-3-6.txt:        cell culture. Author 3 designed, interpreted and supervised
technical/biomed/1471-2377-3-4.txt:            control studies for cell culture are performed:
technical/biomed/1471-2407-2-16.txt:        some cell culture experiments. Author #2 was responsible
technical/biomed/1471-2407-2-16.txt:        participated in cell culture experiments and preparation of
technical/biomed/1471-2407-2-17.txt:          adapted to cell culture and give rise to tumours with the
technical/biomed/1471-2407-2-17.txt:          supernatant of the cell culture lysate after 2 days of
technical/biomed/1471-2458-3-5.txt:        cell culture based detection. The use of filter collection
technical/biomed/1472-6750-1-11.txt:          of the enzyme in the cell culture media over the entire
technical/biomed/1472-6750-1-12.txt:          ES cell culture, gene targeting and
technical/biomed/1472-6750-2-21.txt:          μl) of overnight cell culture was mixed with effector
technical/biomed/1472-6750-3-4.txt:          96-well cell culture plate (8 × 10 3cells per well),
technical/biomed/1472-6750-3-4.txt:          Six-well cell culture plates, coated with poly-
technical/biomed/1472-6793-1-11.txt:        intestinal cell culture model of vitamin D-mediated
technical/biomed/1472-6793-1-11.txt:          cell culture medium is approximately 10 -12mol/L. As
technical/biomed/1472-6793-1-11.txt:          Conditions of cell culture
technical/biomed/1472-6807-1-1.txt:        shown by protein content of cell culture dishes, which is
technical/biomed/1472-6882-1-11.txt:          cell culture medium during cell-mediated cytotoxicity.
technical/biomed/1472-6890-3-2.txt:        drafted the manuscript. HAA prepared cell culture lines and
technical/biomed/1475-2867-2-10.txt:        The results of cell culture and animal studies have
technical/biomed/1475-2875-2-14.txt:          Probes, Eugene, OR. Reagents used in cell culture and
technical/biomed/1475-2891-1-2.txt:          RPMI-1640 medium without phenol red, cell culture
technical/biomed/1475-2891-1-2.txt:          depletion phase). During the course of the cell culture
technical/biomed/1475-4924-1-10.txt:          50 values in cell culture for these
technical/biomed/1476-4598-2-1.txt:          cell culture condition is unlikely to be translated to
technical/biomed/1476-4598-2-1.txt:          function of PDGFR under the cell culture conditions, it
technical/biomed/1476-4598-2-2.txt:        of the fresh tumor samples, we turned to the cell culture
technical/biomed/1476-4598-2-2.txt:        in the nucleus seen in the cell culture.
technical/biomed/1476-4598-2-24.txt:        Author 1 (GN) performed cell culture, MSP and gene
technical/biomed/1476-4598-2-25.txt:          Monolayer cell culture was performed as previously
technical/biomed/1477-7827-1-13.txt:          and utilized as a cell culture positive control. Rat
technical/biomed/1477-7827-1-13.txt:          Amnion fibroblast cell culture
technical/biomed/1477-7827-1-36.txt:        cell culture) they produce neuronal daughter cells to which
technical/biomed/ar68.txt:        exists, and cell culture experiments [ 14, 15, 16, 17]
technical/biomed/ar778.txt:        using nonhematopoietic cell lines or prolonged cell culture
technical/biomed/ar792.txt:          Materials, cells and cell culture
technical/biomed/bcr273.txt:          and activation, both in cell culture and in rats 
technical/biomed/bcr273.txt:          production and activation, both in cell culture and in
technical/biomed/bcr273.txt:          Interestingly, in cell culture, both tamoxifen and
technical/biomed/bcr284.txt:          Development of cell lines and cell culture
technical/biomed/bcr303.txt:          Cell line and cell culture
technical/biomed/bcr45.txt:          Cells and cell culture
technical/biomed/bcr620.txt:        phenomenon of cell culture or that OPN-positive cells have
technical/biomed/bcr631.txt:          in cell culture studies. One complexity in our work is
technical/biomed/gb-2002-3-7-research0036.txt:            (cell culture, mRNA isolation, labeling, hybridization,
technical/biomed/gb-2002-3-7-research0037.txt:          developed in-house were grown in mesothelial cell culture
technical/biomed/gb-2003-4-7-r46.txt:          determined for each xenograft and cell culture profile to
technical/biomed/gb-2003-4-7-r46.txt:          tumors compared to cell culture are highly indicative of
technical/biomed/gb-2003-4-7-r46.txt:        values used in the classifications of cell culture lineage
technical/biomed/gb-2003-4-7-r46.txt:        lineage of all six cell culture profiles, as an Excel
technical/biomed/gb-2003-4-7-r46.txt:        Expression datasets of the cell culture and xenograft
technical/biomed/gb-2003-4-7-r46.txt:        Expression datasets of the cell culture and xenograft
technical/biomed/gb-2003-4-7-r46.txt:        The values used in the classifications of cell culture
technical/biomed/gb-2003-4-7-r46.txt:        lineage of all six cell culture profiles
technical/biomed/gb-2003-4-7-r46.txt:        The values used in the classifications of cell culture
technical/biomed/gb-2003-4-7-r46.txt:        lineage of all six cell culture profiles
technical/biomed/rr191.txt:          cell culture media. Pyruvate conversion into lactate was
```
6.
```
Bluestarr@MacBook-Pro-8 docsearch % grep -w  "differ significantly"  technical/biomed/*.txt
technical/biomed/1471-2148-2-2.txt:          bmr18 do not differ significantly
technical/biomed/1471-2148-3-7.txt:          if they differ significantly from the null hypothesis of
technical/biomed/1471-2148-3-7.txt:          determine whether they differ significantly from the null
technical/biomed/1471-2156-2-12.txt:          In strain 129P3/J, IOP did not differ significantly
technical/biomed/1471-2164-4-4.txt:        transcripts that differ significantly in expression when
technical/biomed/1471-2180-3-13.txt:          ompC differ significantly and the 
technical/biomed/1471-2202-2-5.txt:            neurons/mm 3) do not differ significantly from each
technical/biomed/1471-2202-3-5.txt:        differ significantly in wings or forelegs, for example. The
technical/biomed/1471-2202-4-11.txt:        However, fish and human genes differ significantly in the
technical/biomed/1471-2202-4-5.txt:          not differ significantly in the two taste nerves. Several
technical/biomed/1471-2296-3-18.txt:          impaired fasting glucose did not differ significantly
technical/biomed/1471-2296-3-19.txt:          not differ significantly between non-Hispanic white and
technical/biomed/1471-2334-1-9.txt:          not differ significantly (Table). These data indicate
technical/biomed/1471-2350-4-3.txt:            differ significantly, with two exceptions. The
technical/biomed/1471-244X-2-9.txt:        loss for ADSx did not differ significantly from AD (2.3 vs.
technical/biomed/1472-6874-2-1.txt:        illustrate that the two groups do not differ significantly
technical/biomed/1472-6882-2-10.txt:        gain did not differ significantly from weight gained by LD
technical/biomed/1472-6882-2-10.txt:        Brain weights did not differ significantly, although the
technical/biomed/1472-6904-3-1.txt:          results differ significantly from the model data. Despite
technical/biomed/1475-2875-2-10.txt:            drugs were found to differ significantly by type of
technical/biomed/1475-2883-2-11.txt:        intensity did not differ significantly by sentinel site
technical/biomed/1477-7525-1-10.txt:          differ significantly at pre-intervention in any
technical/biomed/1477-7827-1-31.txt:          antagonists differ significantly between the present
technical/biomed/ar140.txt:          not differ significantly from that in the RASF, but did
technical/biomed/ar140.txt:          differ significantly from that in normal blood ( 
technical/biomed/ar140.txt:          differ significantly from that in RASF, but was
technical/biomed/bcr273.txt:          the staining did not differ significantly from that of
technical/biomed/cc1547.txt:        • Urinary levels of TBARS do not differ significantly
technical/biomed/gb-2001-3-1-research0005.txt:        differ significantly, despite averaging over 20 probe
technical/biomed/gb-2002-3-12-research0072.txt:          i ' values differ significantly
technical/biomed/gb-2002-3-9-research0045.txt:          differ significantly from the other probe and from the
```
Using this command will match the exact word present so if given cell culture it will only return that exact string, so not cell cultures.

7. 
```
Bluestarr@MacBook-Pro-8 docsearch % grep -A 5  "Pyruvate conversion"  technical/biomed/*.txt
technical/biomed/rr191.txt:          cell culture media. Pyruvate conversion into lactate was
technical/biomed/rr191.txt-          measured in 0.2 M Tris-HCl (pH 7.2) buffer in the
technical/biomed/rr191.txt-          presence of sodium pyruvate (0.037 mg/ml, Fisher
technical/biomed/rr191.txt-          Scientific, Fair Lawn, NJ, USA) and the reduced form of
technical/biomed/rr191.txt-          β-nicotinamide adenine dinucleotide (0.057 mg/ml, Sigma)
technical/biomed/rr191.txt-          at 22°C by measuring absorbance at 340 nm. LDH activity
```
8. 
```
Bluestarr@MacBook-Pro-8 docsearch % grep -A 5  "from that in the RASF"  technical/biomed/*.txt
technical/biomed/ar140.txt:          not differ significantly from that in the RASF, but did
technical/biomed/ar140.txt-          differ significantly from that in normal blood ( 
technical/biomed/ar140.txt-          P < 0.001) and RAPB ( 
technical/biomed/ar140.txt-          P < 0.001). The percentage of
technical/biomed/ar140.txt-          cells that produced both IFN-γ and IL-2 (25 ± 1%) did not
technical/biomed/ar140.txt-          differ significantly from that in RASF, but was
```
This command looks for the given string and then prints the n lines that come after it. 

Source: https://www.geeksforgeeks.org/grep-command-in-unixlinux/
