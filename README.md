# MSzadaca
ako, prilikom pokretanja cijele bilježnice, zadnji rezultat, tj, točnost modela bude 44% ili neki drugi broj, a ne 84% kako piše u komentaru ispod,znači da se u liniji: theta = matrix(random_numbers_generator(-0.5, 0.5, 3, 1), dtype=float)
dobila takva theta da se u liniji: parametri = opt.fmin_tnc(func=log_cost, fprime=log_grad, x0=theta, args=(X_exams, y_exams))
parametri = np.array(parametri[0])
događa dijeljenje s 0. Trebalo bi ponovno pokrenuti cijelu bilježnicu. <br>
Također, svi rezultati na koje utječe "random theta" su napisani u bilježnici onako kako su dobiveni u tom trenutku pokretanja bilježnice. Ako se ne dogodi već spomenuto dijeljenje s 0, rezultati funkcija hipoteza mogu se razlikovati u nekoj od decimala jer rezultat ovisi o tome koju thetu ćemo dati za 'initial guess'.
