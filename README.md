# TP_essai
// la classe des tratements// 
public class traitements {
    public traitements() {
    }

    public int[] trier(int[] tab) {
        int taille = tab.length;
        boolean j = false;
        boolean tmp = false;

        for(int i = 0; i < taille; ++i) {
            int var7 = i;

            for(int k = i; k < taille; ++k) {
                if(tab[var7] > tab[k]) {
                    var7 = k;
                }
            }

            int var8 = tab[i];
            tab[i] = tab[var7];
            tab[var7] = var8;
        }

        return tab;
    }

    public int[] iverser(int[] tab) {
        int taille = tab.length;

        for(int i = 0; i < taille - 1; ++i) {
            int interm = tab[i];
            tab[i] = tab[taille - 1 - i];
            tab[taille - 1 - i] = interm;
        }

        return tab;
    }

    public int[] somme(int[] tab1, int[] tab2) throws EgaliteException {
        int taille1 = tab1.length;
        int taille2 = tab2.length;
        int[] res = new int[100];
        boolean i = false;

        for(int var7 = 0; var7 < taille1; ++var7) {
            res[var7] = tab1[var7] + tab2[var7];
        }

        return res;
    }

    public int[] produit2(int[] tab) {
        boolean i = false;

        for(int var3 = 0; var3 < tab.length; ++var3) {
            tab[var3] *= 2;
        }

        return tab;
    }

    public int[] MaxMin(int[] tab) {
        int[] res = new int[2];
        this.trier(tab);
        res[0] = tab[0];
        res[1] = tab[tab.length - 1];
        return res;
    }
}

