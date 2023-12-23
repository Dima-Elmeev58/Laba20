# Laba12
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("Введите путь к текстовому файлу");
            string FilePath = Console.ReadLine();
            if (File.Exists(FilePath))
            {
                string Content = File.ReadAllText(FilePath);
                string NewFile = "new_file.txt";
                File.WriteAllText(NewFile, Content);
                Console.WriteLine("Успешно.");
            }
            else
            {
                Console.WriteLine("Ошибка. Файл не существует.");

            }
        }
    }
}
