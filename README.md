# tableaumultidimentionnel
creation d'un tableau uni, puis multi diementionnel l'un dans l'autre
// Déclaration du tableau uniforme 3x3
int[,] tableauUniforme = new int[3, 3] {
{1, 2, 3},
{2, 3, 4},
{3, 4, 5}
};

// Déclaration du tableau irrégulier 3xn
int[][] tableauIrregulier = new int[3][];

// Remplissage du tableau irrégulier à partir du tableau uniforme
for (int i = 0; i < 3; i++)
{
tableauIrregulier[i] = new int[3 - i];
for (int j = 0; j < 3 - i; j++)
{
tableauIrregulier[i][j] = tableauUniforme[i, j];
}
}

// Affichage du tableau irrégulier
for (int i = 0; i < 3; i++)
{
Console.Write("[" + i + " => [");
for (int j = 0; j < tableauIrregulier[i].Length; j++)
{
Console.Write(tableauIrregulier[i][j]);
if (j < tableauIrregulier[i].Length - 1)
{
Console.Write(", ");
}
}
Console.WriteLine("]]");
}
