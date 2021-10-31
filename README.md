To reproduce, run:

    java -jar maxent.jar EnglishParameters.params

This produces the following trace:

    args=[-features, EnglishFeatures.txt, -corpus, EnglishLearningData.txt, -sigma2, 1.00E+10, -maxGramSize, 3, -minWordLength, 1, -maxWordLength, 12, -train, , -alpha, 0.15, -prune, , -selectFromList, , -test, EnglishTestingData_Scholes.txt, -prePrune, , -doNotAddStarSeg, ]
    Exception in thread "main" java.lang.IndexOutOfBoundsException: Index: -1, Size: 1108
            at java.base/java.util.LinkedList.checkElementIndex(LinkedList.java:559)
            at java.base/java.util.LinkedList.remove(LinkedList.java:529)
            at edu.ucla.fsm.EnumerateNaturalClasses3.apply(EnumerateNaturalClasses3.java:109)
            at edu.ucla.fsm.Alphabet.makeNaturalClasses(Alphabet.java:76)
            at edu.ucla.fsm.Alphabet.<init>(Alphabet.java:58)
            at edu.ucla.fsm.FeatureMatrixReader.apply(FeatureMatrixReader.java:90)
            at edu.ucla.maxent.Maxent.main(Maxent.java:266)
