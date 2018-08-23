---
title: Chamar no Excel a partir de DLL ou XLL
manager: soliver
ms.date: 08/22/2018
ms.audience: Developer
ms.topic: overview
keywords:
- comandos, DLLs [Excel 2007], comandos de chamada para o Excel, passando argumentos às funções da API C [Excel 2007], [Excel 2007], do excel de caixas de diálogo [excel 2007], invocação de invocação com caixas de diálogo, comandos [Excel 2007], acessíveis a partir da DLL/XLL, Excel4 funcionam [ Função de Excel12 do Excel 2007], [Excel 2007], XLCallVer funcionar argumento de operRes [Excel 2007], [Excel 2007], funções [Excel 2007], acessíveis a partir da DLL/XLL, Excel12v funcionam [Excel 2007], somente DLL funciona [Excel 2007], C API [Excel 2007], passando Contagem de argumentos, o argumento [Excel 2007], comandos [Excel 2007], chamando em versões internacionais, somente DLL comandos [Excel 2007], versões internacionais [Excel 2007], chamadas funções e comandos, XLLs [Excel 2007], ligações para Excel, Excel 4v função [ Excel 2007], xlfn argumento [Excel 2007], [Excel 2007], de funções chamando em versões internacionais
localization_priority: Normal
ms.assetid: 616e3def-e4ec-4f3c-bc65-3b92710da1e6
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 996226aa8e01d58edbe9b9a8d6e6996b2453d581
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567703"
---
# <a name="calling-into-excel-from-the-dll-or-xll"></a>Chamar no Excel a partir de DLL ou XLL

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
O Microsoft Excel permite que sua DLL acessar os comandos internos do Excel, funções de planilha e funções de folha de macro. Essas são disponíveis tanto de comandos DLL e funções chamadas a partir do Visual Basic for Applications (VBA) e registrados comandos XLL e funções chamadas diretamente pelo Excel.
  
## <a name="excel4-excel4v-excel12-and-excel12v-functions"></a>Excel4, Excel4v, Excel12 e funções Excel12v

Excel permite que sua DLL acessar as funções e comandos por meio das funções de retorno de chamada [Excel4](excel4-excel12.md), [Excel4v](excel4v-excel12v.md), [Excel12](excel4-excel12.md)e [Excel12v](excel4v-excel12v.md).
  
As funções do **Excel4** e **Excel4v** foram introduzidas no Excel versão 4. Eles funcionam com a estrutura de dados **XLOPER** . Excel 2007 introduziu duas novas funções de retorno de chamada, **Excel12** e **Excel12v**, que funcionam com a estrutura de dados **XLOPER12** . As funções do **Excel4** e **Excel4v** são exportadas pela biblioteca xlcall32, que devem ser incluídos em seu projeto DLL ou XLL. **Excel12** e **Excel12v** estão incluídos no arquivo de origem C++ SDK Xlcall.cpp, que devem ser incluídos em seu projeto, se você deseja acessar a funcionalidade do Excel usando **XLOPER12** estruturas. 
  
O código a seguir mostra os protótipos de função para essas quatro funções. Os três primeiros argumentos são os mesmos, exceto que o segundo argumento é um ponteiro para um **XLOPER** no primeiro par e um ponteiro para **XLOPER12** no segundo par. A convenção de chamada é **cdecl** in **Excel4** e **Excel12** para permitir que as listas de argumentos variável. Nas reticências representa ponteiros para os valores **XLOPER** para **Excel4** e valores de **XLOPER12** para **Excel12**. O número de ponteiros é igual ao valor do parâmetro _contagem_ . 
  
**Todas as versões do Excel**
  
 `int _cdecl Excel4(int xlfn, LPXLOPER operRes, int count,... );`
  
 `int pascal Excel4v(int xlfn, LPXLOPER operRes, int count, LPXLOPER opers[]);`
  
**Iniciando no Excel 2007**
  
 `int _cdecl Excel12(int xlfn, LPXLOPER12 operRes, int count,... );`
  
 `int pascal Excel12v(int xlfn, LPXLOPER12 operRes, int count, LPXLOPER12 opers[]);`
  
Para a DLL poder chamar **Excel4**, **Excel4v**, **Excel12**ou **Excel12v**, Excel deve passar o controle para a DLL. Isso significa que esses retornos de chamada do C API podem ser chamados apenas nos seguintes cenários:
  
- De dentro um comando XLL do Excel foi chamado diretamente ou por meio do VBA.
    
- De dentro de uma função de planilha XLL planilha ou macro que o Excel tem chamado diretamente ou por meio do VBA.
    
Você não pode chamar a API C do Excel nos seguintes cenários:
  
- A partir de um evento de sistema operacional (por exemplo, a partir de função [DllMain](https://docs.microsoft.com/windows/desktop/dlls/dllmain) ). 
    
- De um segmento de plano de fundo que sua DLL criado.
    
### <a name="return-values"></a>Valores de retorno

Todos os quatro dessas funções retornam um valor integer que informa ao chamador se o comando ou a função foi chamado com êxito. Os valores retornados podem ser qualquer um dos seguintes procedimentos:
  
|**Valor retornado**|**Definidos no xlcall. h como**|**Descrição**|
|:-----|:-----|:-----|
|0  <br/> |**xlretSuccess** <br/> |A função ou o comando foi executada com êxito. Isso significa que a execução foi sem erros. Por exemplo, **Excel4** poderia retornar **xlretSuccess** ao chamar a função **Localizar**, embora ele avaliado para **#VALUE!** porque o texto de pesquisa não pôde ser encontrado. Você deve inspecionar o tipo e o valor retornado **XLOPER/XLOPER12** onde isso é uma possibilidade.  <br/> |
|1  <br/> |**xlretAbort** <br/> |Uma macro de comando foi interrompida pelo usuário clicar no botão **Cancelar** ou pressionando a tecla ESC.  <br/> |
|2  <br/> |**xlretInvXlfn** <br/> |A função fornecida ou o código do comando não é válido. Esse erro pode ocorrer quando a função de chamada não tem permissão para chamar a função ou o comando. Por exemplo, uma função de planilha não é possível chamar uma função de informações de folha de macro ou uma função de comando.  <br/> |
|4  <br/> |**xlretInvCount** <br/> |O número de argumentos fornecidos na chamada não está correto.  <br/> |
|8  <br/> |**xlretInvXloper** <br/> |Um ou mais dos valores do argumento **XLOPER** ou **XLOPER12** estão formado incorretamente ou preenchido.  <br/> |
|16  <br/> |**xlretStackOvfl** <br/> |Excel detectado um risco que a operação talvez sua pilha de estouro e, portanto, não tivesse chamado a função.  <br/> |
|32  <br/> |**xlretFailed** <br/> |O comando ou função falhou por uma razão não descrita por um dos outros valores de retorno. Uma operação que exija muita memória, por exemplo, falhará com esse erro. Isso pode acontecer durante uma tentativa de converter uma referência muito grande para uma matriz de **xltypeMulti** usando a função [xlCoerce](xlcoerce.md) .  <br/> |
|64  <br/> |**xlretUncalced** <br/> |A operação tentou recuperar o valor de uma célula não calculada. Para preservar a integridade de recálculo no Excel, funções de planilha não têm permissão para fazer isso. Entretanto, as funções e comandos XLL registrado como funções de folha de macro têm permissão para acessar valores de células não calculadas.  <br/> |
|128  <br/> |**xlretNotThreadSafe** <br/> |(Começando no Excel 2007) Uma função de planilha XLL registrada como thread-safe tentou chamar uma função da API C que não seja thread-safe. Por exemplo, uma função thread-safe não é possível chamar a função XLM **xlfGetCell**.  <br/> |
|256  <br/> |**xlRetInvAsynchronousContext** <br/> |(Começando no Excel 2010) O identificador de função assíncronas é inválido.  <br/> |
|512  <br/> |**xlretNotClusterSafe** <br/> |(Começando no Excel 2010) A chamada não é suportada em clusters.  <br/> |
   
Se a função retornará um dos valores de falha na tabela (ou seja, ele não retorna **xlretSuccess**), o valor de retorno **XLOPER** ou **XLOPER12** também será definido **#VALUE!**. Em certas circunstâncias, por isso pode ser um teste suficiente de sucesso, mas lembre-se de que uma chamada pode retornar ambas as **xlretSuccess** de verificação e **#VALUE!**.
  
Se uma chamada para os resultados da API C no **xlretUncalced** ou **xlretAbort**, seu código DLL ou XLL deve retornar controle para o Excel antes de fazer qualquer outras chamadas de API C (além de chamadas para a função de [xlfree](xlfree.md) para liberar memória alocada para Excel recursos nos valores **XLOPER** e **XLOPER12** ). 
  
### <a name="command-or-function-enumeration-argument-xlfn"></a>Comando ou argumento de enumeração de função: xlfn

O argumento _xlfn_ é o primeiro argumento para o retorno de chamada funciona e é um inteiro assinado de 32 bits. Seu valor deve ser uma das enumerações função ou comando definidas no arquivo de cabeçalho do SDK xlcall. h, conforme mostrado no exemplo a seguir. 
  
```cs
// Excel function numbers. 
#define xlfCount 0
#define xlfIsna 2
#define xlfIserror 3
#define xlfSum 4
#define xlfAverage 5
#define xlfMin 6
#define xlfMax 7
#define xlfRow 8
#define xlfColumn 9
#define xlfNa 10
...
// Excel command numbers. 
#define xlcBeep (0 | xlCommand)
#define xlcOpen (1 | xlCommand)
#define xlcOpenLinks (2 | xlCommand)
#define xlcCloseAll (3 | xlCommand)
#define xlcSave (4 | xlCommand)
#define xlcSaveAs (5 | xlCommand)
#define xlcFileDelete (6 | xlCommand)
#define xlcPageSetup (7 | xlCommand)
#define xlcPrint (8 | xlCommand)
#define xlcPrinterSetup (9 | xlCommand)
...
```

Folha de macro e planilha de todas as funções estão no intervalo de 0 (**xlfCount**) a 0x0fff hexadecimal, embora as mais altas atribuído número no Excel 2013 é 547 decimal, 0x0223 hexadecimal (**xlfFloor_precise**).
  
Todas as funções de comando estão no intervalo entre 0x8000 hexadecimal (**xlcBeep**) por meio de 0x8fff hexadecimal, embora o maior número atribuído no Excel 2013 seja 0x8328 hexadecimal (**xlcHideallInkannots**). Esses são definidos no arquivo de cabeçalho como `(n | xlCommand)` onde `n` é um número decimal, maior ou igual a 0 e **xlCommand** é definido como 0x8000 hexadecimal. 
  
### <a name="invoking-excel-commands-that-use-dialog-boxes"></a>Comandos do Excel que usam caixas de diálogo de invocação

Alguns dos códigos de comando correspondem às ações no Excel que usam caixas de diálogo. Por exemplo, **xlcFileDelete** usa um único argumento: um nome de arquivo ou uma máscara. Isso pode ser chamado com a caixa de diálogo para que o usuário tem a oportunidade de cancelar ou modificar a operação de exclusão. Ele também pode ser chamado sem a caixa de diálogo, caso em que o arquivo ou arquivos são excluídos sem nenhuma interação adicional, supondo que elas existirem, e o chamador tiver permissão. Para chamar esses comandos em seu formulário da caixa de diálogo, a enumeração de comando deve ser combinada usando a operação OR bit a bit com 0x1000 (**xlPrompt**).
  
O exemplo de código a seguir exclui arquivos no diretório atual my_data a máscara de correspondência\*. bak, exibindo uma caixa de diálogo somente se o argumento for true.
  
```cs
bool delete_my_backup_files(bool show_dialog)
{
    XLOPER12 xResult, xFilter;
    xFilter.xltype = xltypeStr;
    xFilter.val.str = L"\014my_data*.bak"; // String length: 14 octal
    int cmd;
    if(show_dialog)
        cmd = xlcFileDelete | xlPrompt;
    else
        cmd = xlcFileDelete;
// xResult should be Boolean TRUE if successful, in which
// case return true; otherwise, false.
    return (Excel12(cmd, &xResult, 1, &xFilter) == xlretSuccess
        && xResult.xltype == xltypeBool
        && xResult.val.xbool == 1);
}
```

### <a name="calling-functions-and-commands-in-international-versions"></a>Chamando funções e comandos em versões internacionais

Você pode configurar o Excel para exibir as funções e os nomes dos comandos XLM em uma variedade de idiomas. Algumas funções e comandos do C API operam em cadeias de caracteres que são interpretadas como nomes de função ou comando. Por exemplo, **xlcFormula** leva um argumento de cadeia de caracteres que se destina a ser colocada em uma célula especificada. Para o add-in trabalhar com todas as configurações de idioma, você pode fornecer os nomes de cadeia de caracteres de inglês e definido o bit 0x2000 (**xlIntl**) na enumeração função ou comando.
  
O exemplo de código a seguir coloca o equivalente do `=SUM(X1:X100)` na célula A2 na planilha ativa. Observe que ele usa a função Framework, **TempActiveRef**, para criar uma referência de externa **XLOPER**temporária. A fórmula aparecerão em A2 no idioma correto determinado de localidade (por exemplo, `=SOMME(X1:X100)` se o idioma for francês). 
  
```cs
int WINAPI InternationlExample(void)
{
    XLOPER12 xSum, xResult;
    xSum.xltype = xltypeStr;
    xSum.val.str = L"\015=SUM(X1:X100)";
    Excel12(xlcFormula | xlIntl, &xResult, 2,
        &xSum, TempActiveRef(2,2,1,1));
    return 1;
}

```

> [!NOTE]
> Como o resultado da chamada para **Excel12** não é necessário, zero (nulo) pode ser passado como o segundo argumento em vez do endereço de **xResult**. Isso é mais discutido na próxima seção. 
  
### <a name="dll-only-functions-and-commands"></a>Comandos e funções somente DLL

Excel oferece suporte a um pequeno número de funções que só são acessíveis por um DLL ou XLL. Esses são definidos no arquivo de cabeçalho como `(n | xlSpecial)` onde `n` é um número decimal, maior ou igual a 0 e `xlSpecial` é definido como 0x4000 hexadecimal. Essas funções são listadas na tabela a seguir e documentadas na [Referência do API de função](excel-xll-sdk-api-function-reference.md).
  
||||
|:-----|:-----|:-----|
|[xlFree](xlfree.md) <br/> |0 | xlSpecial  <br/> |Libera os recursos de memória alocada para Excel.  <br/> |
|[xlStack](xlstack.md) <br/> |1 | xlSpecial  <br/> |Retorna o espaço livre na pilha de Excel.  <br/> |
|[xlCoerce](xlcoerce.md) <br/> |2 | xlSpecial  <br/> |Converte entre tipos **XLOPER** e **XLOPER12**  <br/> |
|[xlSet](xlset.md) <br/> |3 | xlSpecial  <br/> |Fornece um método rápido de definir valores de célula.  <br/> |
|[xlSheetId](xlsheetid.md) <br/> |4 | xlSpecial  <br/> |Obtém um nome de planilha a partir de sua identificação de interno.  <br/> |
|[xlSheetNm](xlsheetnm.md) <br/> |5 | xlSpecial  <br/> |Obtém uma ID de planilha interna de seu nome.  <br/> |
|[xlAbort](xlabort.md) <br/> |6 | xlSpecial  <br/> |Verifica se o usuário clicou no botão **Cancelar** ou pressionada a tecla ESC.  <br/> |
|[xlGetInst](xlgetinst.md) <br/> |7 | xlSpecial  <br/> |Obtém o identificador de instância do Excel.  <br/> |
|[xlGetHwnd](xlgethwnd.md) <br/> |8 | xlSpecial  <br/> |Obtém o identificador da janela principal do Excel.  <br/> |
|[xlGetName](xlgetname.md) <br/> |9 | xlSpecial  <br/> |Obtém o nome de arquivo e o caminho da DLL.  <br/> |
|[xlEnableXLMsgs](xlenablexlmsgs.md) <br/> |10 | xlSpecial  <br/> |Essa função foi preterida e não são mais precisa ser chamado.  <br/> |
|[xlDisableXLMsgs](xldisablexlmsgs.md) <br/> |11 | xlSpecial  <br/> |Essa função foi preterida e não são mais precisa ser chamado.  <br/> |
|[xlDefineBinaryName](xldefinebinaryname.md) <br/> |12 | xlSpecial  <br/> |Define um nome de armazenamento persistente de binários.  <br/> |
|[xlGetBinaryName](xlgetbinaryname.md) <br/> |13 | xlSpecial  <br/> |Obtém os dados de um nome armazenamento persistente de binários.  <br/> |
   
## <a name="return-value-xloperxloper12-operres"></a>Retornar o valor XLOPER/XLOPER12: operRes

O argumento _operRes_ é o segundo argumento para os retornos de chamada e um ponteiro para um **XLOPER** (**Excel4** e **Excel4v**) ou **XLOPER12** (**Excel12** e **Excel12v**). Depois de uma chamada bem sucedida, ele contém o valor de retorno da função ou do comando. **operRes** pode ser definido como zero (ponteiro NULL), se nenhum valor de retorno é necessário. O conteúdo anterior do **operRes** será sobrescrito para que qualquer memória apontada anteriormente deve ser liberada antes para a chamada para evitar vazamento de memória. 
  
Se a função ou o comando não pode ser chamado (por exemplo, se os argumentos são incorretos), o **operRes** será definida como o erro **#VALUE!**. Um comando sempre retorna **booleano** **TRUE** se ele for bem-sucedido ou **FALSE** se ela falhou ou o usuário cancelou a ele. 
  
## <a name="number-of-subsequent-arguments-count"></a>Número de argumentos subsequentes: contagem

O argumento _count_ é o terceiro argumento para os retornos de chamada e um inteiro assinado de 32 bits. Ela deve ser definida como o número de argumentos subsequentes, contado a partir de 1. Se um comando ou função não assumir nenhum argumento, ela deve ser definida como zero. No Microsoft Office Excel 2003, o número máximo de argumentos que pode ser realizadas por qualquer função é 30, embora a maioria levar a menos que isso. Iniciando no Excel 2007, o número máximo de argumentos que pode ser realizadas por qualquer função aumentou a 255. 
  
Com **Excel4** e **Excel12**, _count_ é o número de ponteiros para **XLOPER** ou **XLOPER12** valores que estão sendo passados. Você deve ser muito cuidado para não passar essa _contagem_ de menos argumentos que o valor é definido como. Isso resultará em Excel lendo com antecedência à pilha de e tentar processar valores **XLOPER** ou **XLOPER12** inválidos, que podem causar uma falha de aplicativo. 
  
Com **Excel4v** e **Excel12v**, _count_ é o tamanho da matriz de ponteiros para valores **XLOPER** ou **XLOPER12** que está sendo passado como o argumento seguinte e final. Novamente, você deve ser muito cuidado para não passe uma matriz de menor que elementos de _contagem_ no tamanho, como isso resultará nos limites da matriz sendo saturação. 
  
## <a name="passing-arguments-to-c-api-functions"></a>Passagem de argumentos para funções da API C

**Excel4** e **Excel12** levam comprimento variável listas de argumentos, após _contagem_, que são interpretadas como ponteiros para valores **XLOPER** e **XLOPER12** , respectivamente. **Excel4v** e **Excel12v** entram em um único argumento, após _contagem_, que é um ponteiro para uma matriz de ponteiros para valores **XLOPER** no caso de **Excel4v**e **XLOPER12** valores no caso de **Excel12v**.
  
Formulários de matriz, **Excel4v** e **Excel12v**, permitem que você codificar uma chamada para a API C corretamente quando o número de argumentos é a variável. O exemplo a seguir mostra uma função que usa uma matriz de tamanho variável de números e usa as funções de planilha do Excel, por meio da API C, para calcular a soma, média, mínima e máxima. 
  
```cs
void Excel12v_example(double *dbl_array, int size, double &sum, double &average, double &min, double &max)
{
// 30 is the limit in Excel 2003. 255 is the limit in Excel 2007.
// Use the lower limit to be safe, although it is better to make
// the function version-aware and use the correct limit.
    if(size < 1 || size > 30)
        return;
// Create an array of XLOPER12 values.
    XLOPER12 *xOpArray = (XLOPER12 *)malloc(size * sizeof(XLOPER12));
// Create an array of pointers to XLOPER12 values.
    LPXLOPER12 *xPtrArray =
        (LPXLOPER12 *)malloc(size * sizeof(LPXLOPER12));
// Initialize and populate the array of XLOPER12 values
// and set up the pointers in the pointer array.
    for(int i = 0; i < size; i++)
    {
        xOpArray[i].xltype = xltypeNum;
        xOpArray[i].val.num = dbl_array[i];
        xPtrArray[i] = xOpArray + i;
    }
    XLOPER12 xResult;
    int retval;
    int fn[4] = {xlfSum, xlfAverage, xlfMin, xlfMax};
    double *result_ptr[4] = {&sum, &average, &min, &max};
    for(i = 0; i < 4; i++)
    {
        retval = Excel12v(fn[i], &xResult, size, xPtrArray);
        if(retval == xlretSuccess && xResult.xltype == xltypeNum)
            *result_ptr[i] = xResult.val.num;
    }
    free(xPtrArray);
    free(xOpArray);
}

```

Substituindo referências aos valores **XLOPER12** com **XLOPER**e **Excel12v** com **Excel4v**, no código precedente for resultar em uma função que funcionaria com todas as versões do Excel. Essa operação das funções do Excel **soma**, **média**, **MIN**e **MAX** é tão simple que seria mais eficiente codificá-los em C e evitar a sobrecarga de preparar os argumentos e ligações para o Excel. No entanto, muitas das funções do que Excel contém são mais complexas, tornando essa abordagem útil em alguns casos. 
  
O tópico [xlfRegister](xlfregister-form-1.md) fornece outro exemplo de como trabalhar com **Excel4v** e **Excel12v**. Ao registrar uma função de planilha XLL, você pode fornecer uma cadeia de caracteres descritiva para cada argumento usado na caixa de diálogo **Colar função** . Portanto, o número de argumentos total sendo fornecido para **xlfRegister** depende do número de argumentos que leva sua função XLL e irá variar de uma função para a próxima. 
  
Onde você sempre chamar uma função do C API ou comando com o mesmo número de argumentos, você deseja evitar a etapa extra de criação de uma matriz de ponteiros para os argumentos. Nesses casos, é mais simples e limpo usar **Excel4** e **Excel12**. Por exemplo, durante o registro de comandos e funções XLL, você precisará fornecer o nome de arquivo e caminho completo da DLL ou XLL. Você pode obter o nome de arquivo em uma chamada para **xlfGetName** e liberá-la com uma chamada para **xlFree**, conforme mostrado no exemplo a seguir para **Excel4** e **Excel12**.
  
```cs
XLOPER xDllName;
if(Excel4(xlfGetName, &xDllName, 0) == xlretSuccess)
{
    // Use the name, and 
    // then free the memory that Excel allocated for the string.
    Excel4(xlFree, 0, 1, &xDllName);
}
XLOPER12 xDllName;
if(Excel12(xlfGetName, &xDllName, 0) == xlretSuccess)
{
    // Use the name, and
    // then free the memory that Excel allocated for the string.
    Excel12(xlFree, 0, 1, &xDllName);
}

```

Na prática, a função, **Excel12v_example**, poderia ser codificada com mais eficiência, criando um único **xltypeMulti** **XLOPER12** argumento e chamando a API C usando-se **Excel12**, conforme mostrado no exemplo a seguir.
  
```cs
void Excel12_example(double *dbl_array, int size, double &sum, double &average, double &min, double &max)
{
// In this implementation, the upper limit is the largest
// single column array (equals 2^20, or 1048576, rows in Excel 2007).
    if(size < 1 || size > 1048576)
        return;
// Create an array of XLOPER12 values.
    XLOPER12 *xOpArray = (XLOPER12 *)malloc(size * sizeof(XLOPER12));
// Create and initialize an xltypeMulti array
// that represents a one-column array.
    XLOPER12 xOpMulti;
    xOpMulti.xltype = xltypeMulti;
    xOpMulti.val.array.lparray = xOpArray;
    xOpMulti.val.array.columns = 1;
    xOpMulti.val.array.rows = size;
// Initialize and populate the array of XLOPER12 values.
    for(int i = 0; i < size; i++)
    {
        xOpArray[i].xltype = xltypeNum;
        xOpArray[i].val.num = dbl_array[i];
    }
    XLOPER12 xResult;
    int fn[4] = {xlfSum, xlfAverage, xlfMin, xlfMax};
    double *result_ptr[4] = {&sum, &average, &min, &max};
    for(i = 0; i < 4; i++)
    {
        Excel12(fn[i], &xResult, 1, &xOpMulti);
        if(xResult.xltype == xltypeNum)
            *result_ptr[i] = xResult.val.num;
    }
    free(xOpArray);
}

```

> [!NOTE]
> Nesse caso, o valor de retorno do **Excel12** será ignorado. Em vez disso, o código verifica a que o retornado **XLOPER12** é **xltypeNum** para determinar se a chamada foi bem-sucedida. 
  
## <a name="xlcallver"></a>XLCallVer

Além dos retornos de chamada **Excel4**, **Excel4v**, **Excel12**e **Excel12v**, Excel exporta uma função **XLCallVer**, que retorna a versão da API C em execução no momento.
  
O protótipo de função é da seguinte maneira:
  
 `int pascal XLCallVer(void);`
  
Você pode chamar essa função, que é thread-safe, de qualquer comando XLL ou função.
  
No Excel 97 até o Excel 2003, **XLCallVer** retorna 1280 = 0x0500 hex = 5 x 256, que indica a versão 5 do Excel. Iniciando no Excel 2007, ele retorna hex 3072 = 0x0c00 = 12 x 256, que indica da mesma forma versão 12.
  
Embora você possa usar isso para determinar se a nova API C está disponível em tempo de execução, talvez você prefira detectar a versão em execução do Excel usando `Excel4(xlfGetWorkspace, &version, 1, &arg)`, onde `arg` é um **XLOPER** numérico definido como 2. A função retornará uma cadeia de caracteres **XLOPER**, versão, que pode ser forçada a um inteiro. O motivo para contar com a versão do Excel, em vez da versão do C API é que não existem diferenças entre o Excel 2000, Excel 2002 e Excel 2003 que seu suplemento talvez também precise detectar. Por exemplo, foram feitas alterações na precisão de algumas das funções estatísticas.
  
## <a name="see-also"></a>Confira também

- [Criar XLLs](creating-xlls.md)  
- [Acessar o código de XLL no Excel](accessing-xll-code-in-excel.md)  
- [Excel XLL SDK API Function Reference](excel-xll-sdk-api-function-reference.md)  
- [Retorno de chamada da API de C: funções Excel4, Excel12](c-api-callback-functions-excel4-excel12.md)  
- [Desenvolvimento de XLLs do Excel](developing-excel-xlls.md)

