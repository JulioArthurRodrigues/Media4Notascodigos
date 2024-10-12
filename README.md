# Media4Notascodigos

double n1, n2, n3, n4, media;
string resultado;
ConsoleColor corResultado;

Console.WriteLine("-- Média --\n");
Console.WriteLine("Digite as suas notas abaixo.");

Console.Write("Nota 1: ");
n1 = Convert.ToDouble(Console.ReadLine());

Console.Write("Nota 2: ");
n2 = Convert.ToDouble(Console.ReadLine());

Console.Write("Nota 3: ");
n3 = Convert.ToDouble(Console.ReadLine());

Console.Write("Nota 4: ");
n4 = Convert.ToDouble(Console.ReadLine());

Console.WriteLine();

if (n1 < 0 || n1 > 10
 || n2 < 0 || n2 > 10
 || n3 < 0 || n3 > 10
 || n4 < 0 || n4 > 10)
{
    Console.WriteLine("Digite somente notas entre 0 e 10.");
}
else
{
    media = (n1 + n2 + n3 + n4) / 4;

    if (media < 5)
    {
        corResultado = ConsoleColor.Red;
        resultado = "Reprovado";
        
    }
    else if (media > 6)
    {
        corResultado = ConsoleColor.Blue;
        resultado = "Aprovado";
       
    }
    else
    {
        corResultado = ConsoleColor.Yellow;
        resultado = "Em recuperação";
        
    }

    Console.Write($"Você ficou com média {media:N1}. Resultado: {resultado}");
    Console.ForegroundColor = corResultado;
    Console.WriteLine($"{resultado}");
    Console.ResetColor();
}
