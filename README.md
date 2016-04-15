How to install locally:

    sage-develop setup.py develop --user

How to test:

    sage-develop -t --force-lib sage_modabvar

WARNING: We must go through *all* doctests and ensure that they import the
functions being tested directly from sage_modabvar, so that the code here
is being tested, not the code in the Sage library.


Always use:

    sage-develop

Further test:

    sage: from sage_modabvar import J0
    sage: A = J0(43)[1]; B,_ = A.quotient(A.torsion_subgroup(2)); End(B).gens()


New test cases:

    sage: from sage_modabvar import J0
    sage: J = J0(11); B = J.degeneracy_map(33,1).codomain()
    sage: type(B)
    # problem is that this is "getting out of the space"

New one:

    sage: A = ModularSymbols(33).cuspidal_submodule().abelian_variety()
    # need to replace by some function.


New one:

            sage: sage.modular.abvar.abvar.ModularAbelianVariety_modsym_abstract._modular_symbols(A)

