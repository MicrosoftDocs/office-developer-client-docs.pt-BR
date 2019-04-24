---
title: Chamar no Excel a partir de DLL ou XLL
manager: soliver
ms.date: 08/22/2018
ms.audience: Developer
ms.topic: overview
keywords:
- caixas de diálogo [excel 2007], chamando comandos excel, DLLs [Excel 2007], chamando para o Excel, passando argumentos para funções da API C [Excel 2007], comandos [Excel 2007], invocando caixas de diálogo, comandos [Excel 2007], acessíveis da DLL / XLL, função Excel4 [Excel 2007], função Excel12 [Excel 2007], função XLCallVer [Excel 2007], argumento operRes [Excel 2007], funções [Excel 2007], acessíveis da DLL / XLL, função Excel12v [Excel 2007 ], Somente funções DLL [Excel 2007], API C [Excel 2007], passando argumentos, argumento de contagem [Excel 2007], comandos [Excel 2007], chamadas em versões internacionais, comandos somente DLL [Excel 2007], versões internacionais [Excel 2007], chamando funções e comandos, XLLs [Excel 2007], chamando em Excel, função Excel 4v [Excel 2007], argumento xlfn [Excel 2007], funções [Excel 2007], chamando em versões internacionais
ms.assetid: 616e3def-e4ec-4f3c-bc65-3b92710da1e6
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
localization_priority: Priority
ms.openlocfilehash: 8f2b63ba84b0a78bbf317c284913a8ec0986436f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304155"
---
# <a name="calling-into-excel-from-the-dll-or-xll"></a>Chamar no Excel a partir de DLL ou XLL

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
O Microsoft Excel permite que sua DLL acesse comandos incorporados do Excel, funções de planilha e funções de folha de macro. Eles estão disponíveis em comandos e funções da DLL chamados do Visual Basic for Applications (VBA) e de comandos e funções XLL registrados, chamados diretamente pelo Excel.
  
## <a name="excel4-excel4v-excel12-and-excel12v-functions"></a>Funções Excel4, Excel4v, Excel12 e Excel12v 

O Excel permite que sua DLL acesse os comandos e funções por meio das funções de retorno de chamada [Excel4](excel4-excel12.md), [Excel4v](excel4v-excel12v.md), [Excel12](excel4-excel12.md), e [Excel12v](excel4v-excel12v.md).
  
As funções**Excel4** e **Excel4v** foram introduzidas na versão 4. Elas funcionam com a estrutura de dados **XLOPER**. O Excel 2007 introduziu duas funções novas de retorno de chamada, **Excel12** e **Excel12v**, que funcionam com a estrutura de dados **XLOPER12**. As funções **Excel4** e **Excel4v**são exportadas pela biblioteca Xlcall32.lib, que deve ser incluída no seu projeto DLL ou XLL. **Excel12** e **Excel12v** estão incluídas no arquivo de origem do SDK C ++ Xlcall.cpp, que deve ser incluído no seu projeto se você deseja acessar a funcionalidade do Excel usando as estruturas **XLOPER12**. 
  
O código a seguir mostra os protótipos função dessas quatro funções. Os três primeiros argumentos são iguais, exceto pelo fato de que o segundo argumento é um ponteiro para um **XLOPER** no primeiro par e o ponteiro para um **XLOPER12** no segundo par. A convenção de chamada é **cdecl** no **Excel4** e **Excel12** para permitir que o argumento variável listas. As reticências representam ponteiros para os valores **XLOPER** para **Excel4** e valores **XLOPER12** para **Excel12**. O número de sugestões é igual ao valor do parâmetro _contagem_. 
  
**Todas as versões do Excel**
  
 `int _cdecl Excel4(int xlfn, LPXLOPER operRes, int count,... );`
  
 `int pascal Excel4v(int xlfn, LPXLOPER operRes, int count, LPXLOPER opers[]);`
  
**Começando no Excel 2007**
  
 `int _cdecl Excel12(int xlfn, LPXLOPER12 operRes, int count,... );`
  
 `int pascal Excel12v(int xlfn, LPXLOPER12 operRes, int count, LPXLOPER12 opers[]);`
  
Para a DLL fazer chamadas **Excel4**, **Excel4v**, **Excel12**, ou **Excel12v**, o Excel deve passar o controle para a DLL. Isso significa que esses retornos de chamada da API C podem ser chamados apenas nos seguintes cenários:
  
- De dentro de um comando XLL que o Excel chamou diretamente ou via VBA.
    
- De dentro de uma planilha XLL ou função de folha de macro que o Excel chamou diretamente ou via VBA.
    
Você não pode chamar o C API do Excel nas seguintes situações:
  
- De um evento do sistema operacional (por exemplo, função [DllMain](https://docs.microsoft.com/windows/desktop/dlls/dllmain)). 
    
- De um thread de segundo plano que sua DLL criou.
    
### <a name="return-values"></a>Valores de retorno

Todas as quatro funções retornam um valor inteiro que informa ao chamador se a função ou comando foi chamado com sucesso. Os valores retornados podem ser um destes procedimentos:
  
|**Valor de retorno**|**Estipulados em xlcall. h como**|**Descrição**|
|:-----|:-----|:-----|
|0  <br/> |**xlretSuccess** <br/> |A função ou comando foi executada com êxito. Isso significa que a execução foi livre de erros. Por exemplo, **Excel4** pode retornar **xlretSuccess** ao chamar a função **FIND**, embora avaliado como **#VALUE!** porque não foi possível localizar o texto de pesquisa. Você deve inspecionar o tipo e o valor do **XLOPER/XLOPER12** em que esta é uma possibilidade.  <br/> |
|1  <br/> |**xlretAbort** <br/> |Uma macro de comando foi interrompida pelo usuário clicando no botão**Cancelar** ou pressionando a tecla ESC.  <br/> |
|2  <br/> |**xlretInvXlfn** <br/> |A função fornecida ou código de comando não é válido. Este erro pode ocorrer quando a função de chamadas não tem permissão para ligar para o comando ou função. Por exemplo, uma função de planilha não pode chamar uma função de informações de folha de macro ou uma função de comando.  <br/> |
|4  <br/> |**xlretInvCount** <br/> |O número de argumentos fornecido com a chamada não está correto.  <br/> |
|8  <br/> |**xlretInvXloper** <br/> |Um ou mais dos valores do argumento **XLOPER** ou **XLOPER12** não são adequadamente formados ou preenchidos.  <br/> |
|16  <br/> |**xlretStackOvfl** <br/> |O Excel detectou o risco de a operação poder exceder sua pilha e, portanto, não chamou a função.  <br/> |
|32  <br/> |**xlretFailed** <br/> |O comando ou função falhou por um motivo não descrito por um dos outros valores de retorno. Uma operação que exigiria muita memória, por exemplo, falharia com esse erro. Isso pode ocorrer durante a tentativa de converter uma vasta referência a uma matriz **xltypeMulti** matriz usando a função [xlCoerce](xlcoerce.md).  <br/> |
|64  <br/> |**xlretUncalced** <br/> |A operação tentou recuperar o valor de uma célula não calculada. Para preservar a integridade de recálculo no Excel, as funções de planilha não são autorizadas a fazer isso. No entanto, os comandos e funções XLL registrados como funções de folha de macro têm permissão para acessar valores de célula não calculados.  <br/> |
|128  <br/> |**xlretNotThreadSafe** <br/> |(Começando no Excel 2007) Uma função de planilha XLL registrada como thread-safe tentou chamar uma função da API C que não é thread-safe. Por exemplo, uma função de threads não pode chamar a função XLM **xlfGetCell**.  <br/> |
|256  <br/> |**xlRetInvAsynchronousContext** <br/> |(Começando no Excel 2010) O identificador de função assíncrona é inválido.  <br/> |
|512  <br/> |**xlretNotClusterSafe** <br/> |(Começando no Excel 2010) Não há suporte para a chamada em clusters.  <br/> |
   
Se a função retorna um dos valores de falha na tabela (ou seja, ela não retorna **xlretSuccess**), o valor de retorno **XLOPER** ou **XLOPER12**  também será definido como **#VALUE!**. Em certas circunstâncias, verificar isso pode ser um teste de sucesso, mas você deve observar que uma chamada pode retornar **xlretSuccess** e **#VALUE!**.
  
Se uma chamada de API C resulta em um **xlretUncalced** ou **xlretAbort**, o código DLL ou XLL deve retornar o controle para o Excel antes de fazer quaisquer outras chamadas de API C (diferente de chamadas para a função [xlfree ](xlfree.md) para liberar recursos de memória Excel alocados nos valores **XLOPER** e **XLOPER12**). 
  
### <a name="command-or-function-enumeration-argument-xlfn"></a>Argumento de Enumeração de Comando ou Função: xlfn

O argumento _xlfn_ é o primeiro argumento para as funções de retorno de chamada e é um inteiro assinado de 32 bits. Seu valor deve ser uma das enumerações de função ou comando definidas no arquivo de cabeçalho do SDK Xlcall.h, conforme mostrado no exemplo a seguir. 
  
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

Todas as funções de planilha e folha de macro estão no intervalo de 0 (**xlfCount**) a 0x0fff hexadecimal, embora o maior número atribuído no Excel 2013 seja decimal 547, 0x0223 hexadecimal. (**xlfFloor_precise**).
  
Todas as funções de comando estão no intervalo de 0x8000 hexadecimal (**xlcBeep**) em 0x8fff hexadecimal, embora o maior número atribuído no Excel 2013 é 0x8328 hexadecimal (**xlcHideallInkannots** ). Estes são definidos no arquivo de cabeçalho como `(n | xlCommand)` onde `n` é um número decimal maior ou igual a 0 e **xlCommand** é definido como 0x8000 hexadecimal. 
  
### <a name="invoking-excel-commands-that-use-dialog-boxes"></a>Invocando comandos do Excel que usam caixas de diálogo

Alguns códigos de comando correspondem à ações no Excel que usam caixas de diálogo. Por exemplo, **xlcFileDelete** tem um argumento único: um nome de arquivo ou máscara. Isso pode ser chamado com a caixa de diálogo para que o usuário tenha a oportunidade de cancelar ou modificar a operação de exclusão. Ele também pode ser chamado sem a caixa de diálogo, caso em que o arquivo ou arquivos são excluídos sem qualquer interação adicional, supondo que eles existam e o chamador tenha permissão. Para chamar esses comandos em sua forma de caixa de diálogo, a enumeração de comando deve ser combinada usando a operação OR bit a bit com 0x1000 (**xlPrompt**).
  
O exemplo de código a seguir exclui arquivos no diretório atual que correspondem à máscara my_data\*.bak, exibindo uma caixa de diálogo apenas se o argumento for verdadeiro.
  
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

### <a name="calling-functions-and-commands-in-international-versions"></a>Funções de Chamada e Comandos em Versões Internacionais

Você pode configurar o Excel para exibir os nomes dos comandos e funções XLM em vários idiomas. Alguns comandos e funções da API C operam em cadeias de caracteres que são interpretadas como nomes de funções ou comandos. Por exemplo, **xlcFormula** tem um argumento de cadeia de caracteres que deve ser colocado em uma célula especificada. Para o suplemento trabalhar com todas as configurações de idioma, você pode fornecer os nomes de cadeia de inglês e definir bits 0x2000 (**xlIntl**) na função ou comando de enumeração.
  
O exemplo a seguir coloca o equivalente a `=SUM(X1:X100)` na célula A2 da planilha ativa. Observe que a função de estrutura **TempActiveRef** é usada para criar uma referência externa temporária **XLOPER**. A fórmula aparecerá em A2 no idioma determinado pelo código de idioma correto (por exemplo `=SOMME(X1:X100)`, se o idioma for francês). 
  
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
> Como o resultado da chamada para o **Excel12** não é necessário, zero (NULL) pode ser passado como segundo argumento em vez do endereço de **xResult**. Isso é mais abordado na próxima seção. 
  
### <a name="dll-only-functions-and-commands"></a>Comandos e funções somente DLL

O Excel suporta um pequeno número de funções que só podem ser acessadas por uma DLL ou XLL. Estes são definidos no arquivo como cabeçalho `(n | xlSpecial)` onde `n` é um número decimal maior ou igual a 0 e `xlSpecial` é definido como 0x4000 hexadecimal. Essas funções estão listadas na tabela a seguir e documentadas em [referência da API de função](excel-xll-sdk-api-function-reference.md).
  
||||
|:-----|:-----|:-----|
|[xlFree](xlfree.md) <br/> |0 | xlSpecial  <br/> |Libera recursos de memória alocados no Excel.  <br/> |
|[xlStack](xlstack.md) <br/> |1 | xlSpecial  <br/> |Retorna o espaço livre na pilha do Excel.  <br/> |
|[xlCoerce](xlcoerce.md) <br/> |2 | xlSpecial  <br/> |Converte entre os tipos **XLOPER** e **XLOPER12**  <br/> |
|[xlSet](xlset.md) <br/> |3 | xlSpecial  <br/> |Fornece um método rápido para definir valores de células.  <br/> |
|[xlSheetId](xlsheetid.md) <br/> |4 | xlSpecial  <br/> |Obtém um nome de planilha a partir do ID interno.  <br/> |
|[xlSheetNm](xlsheetnm.md) <br/> |5 | xlSpecial  <br/> |Obtém um ID interno da planilha de seu nome..  <br/> |
|[xlAbort](xlabort.md) <br/> |6 | xlSpecial  <br/> |Verifica se o usuário clica no botão **Cancelar** ou pressiona a tecla ESC.  <br/> |
|[xlGetInst](xlgetinst.md) <br/> |7 | xlSpecial  <br/> |Obtém a alça de instância do Excel.  <br/> |
|[xlGetHwnd](xlgethwnd.md) <br/> |8 | xlSpecial  <br/> |Obtém o identificador de janela principal do Excel.  <br/> |
|[xlGetName](xlgetname.md) <br/> |9 | xlSpecial  <br/> |Obtém o caminho e o nome de arquivo da DLL.  <br/> |
|[xlEnableXLMsgs](xlenablexlmsgs.md) <br/> |10 | xlSpecial  <br/> |Esta função é substituída e não precisa mais ser chamada.  <br/> |
|[xlDisableXLMsgs](xldisablexlmsgs.md) <br/> |11 | xlSpecial  <br/> |Esta função é substituída e não precisa mais ser chamada.  <br/> |
|[xlDefineBinaryName](xldefinebinaryname.md) <br/> |12 | xlSpecial  <br/> |Define um nome de armazenamento binário persistente.  <br/> |
|[xlGetBinaryName](xlgetbinaryname.md) <br/> |13 | xlSpecial  <br/> |Obtém os dados de um nome de armazenamento binário persistente.  <br/> |
   
## <a name="return-value-xloperxloper12-operres"></a>Retorna o valor oper/XLOPER12: operRes

O argumento _operRes_ é o segundo argumento para os retornos de chamada e é um ponteiro para uma **XLOPER** (**Excel4** e **Excel4v**) ou** XLOPER12** (**Excel12** e **Excel12v**). Após uma chamada bem-sucedida, ele contém o valor de retorno da função ou comando. **operRes** pode ser definida como zero (ponteiro nulo) se o valor de retorno for necessário. O conteúdo anterior de **operRes** é sobrescrito para que qualquer memória anteriormente apontada seja liberada antes da chamada para evitar vazamentos de memória. 
  
Se o comando ou a função não pode ser chamado (por exemplo, se os argumentos estão incorretos), **operRes** está definido para o erro **#VALUE!**. Um comando sempre retorna **Booleano** **TRUE** se for bem-sucedido, ou **FALSE** se tiver falhado ou for cancelado pelo usuário. 
  
## <a name="number-of-subsequent-arguments-count"></a>Número de argumentos subsequentes: contagem

O argumento _contagem_ é o terceiro argumento para o retorno de chamada e é um inteiro assinado de 32 bits. Deve ser definido para o número de argumentos subsequentes, contando a partir de 1. Se uma função ou comando não tiver argumentos, ele deverá ser definido como zero. No Microsoft Office Excel 2003, o número máximo de argumentos que qualquer função pode levar é 30, embora a maioria leve menos do que isso. A partir do Excel 2007, o número máximo de argumentos que qualquer função pode levar aumentou para 255. 
  
Com **Excel4** e **Excel12**, _contagem_ é o número de sugestões para valores **XLOPER** ou **XLOPER12** que estão sendo passados. Você deve ter muito cuidado para não transmitir menos argumentos do que o valor para o qual a _contagem_ está configurada. Isso resultaria na leitura do Excel adiante na pilha e na tentativa de processar valores **XLOPER** ou **XLOPER12** inválidos, o que poderia causar uma falha no aplicativo. 
  
Com **Excel4v** e **Excel12v**, _contagem_ é o tamanho da matriz dos ponteiros para os valores **XLOPER** ou **XLOPER12**que está sendo passado como o próximo e último argumento. Novamente, você deve ter muito cuidado para não transmitir uma matriz menor do que o elemento _contagem_ em tamanho, pois isso fará com que os limites da matriz sejam excedidos. 
  
## <a name="passing-arguments-to-c-api-functions"></a>Passando Argumentos para Funções da API C

O **Excel4** e o **Excel12** usam listas de argumentos de tamanho variável, após _contagem_, que são interpretadas como ponteiros para os valores **XLOPER** e **XLOPER12**, respectivamente. **Excel4v** e **Excel12v** fazer um argumento único, após _contagem_, que é um ponteiro para uma matriz de ponteiros para valores **XLOPER** no caso do**Excel4v**e valores**XLOPER12** no caso do **Excel12v**.
  
Os formulários de matriz **Excel4v** e **Excel12v**, 
permite que você codifique uma chamada para a API C de forma limpa quando o número de argumentos for variável. O exemplo a seguir mostra uma função que usa uma matriz de números de tamanho variável e usa funções de planilha do Excel, por meio da API C, para calcular a soma, a média, o mínimo e o máximo. 
  
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

Substituindo referências a valores **XLOPER12** com  **XLOPER**, e **Excel12v** com **Excel4v**, no código anterior resultaria em um função que funcionaria com todas as versões do Excel. Essa operação das funções do Excel **SUM**, **AVERAGE**, **MIN** e **MAX** é tão simples que seria mais eficiente codificá-las em C e evitar a sobrecarga ao preparar os argumentos e chamar o Excel. No entanto, muitas das funções que o Excel contém são mais complexas, tornando essa abordagem útil em alguns casos. 
  
O tópico [xlfRegister](xlfregister-form-1.md) fornece outro exemplo de trabalho com **Excel4v** e **Excel12v**. Ao registrar uma função de planilha XLL, você pode fornecer uma cadeia de caracteres descritiva para cada argumento que é usado na caixa de diálogo **Colar função**. Portanto, o número total de argumentos fornecidos para o **xlfRegister** depende do número de argumentos que sua função XLL usa e varia de uma função para outra. 
  
Onde você sempre chama uma função ou um comando da API C com o mesmo número de argumentos, você deseja evitar a etapa extra de criar uma matriz de ponteiros para esses argumentos. Nesses casos, é mais simples e mais limpo usar **Excel4** e **Excel12**. Por exemplo, ao registrar funções e comandos XLL, você precisa fornecer o caminho completo e o nome do arquivo da DLL ou XLL. Você pode obter o nome do arquivo em uma chamada de **xlfGetName** e, em seguida, soltar com uma chamada ao **xlFree**, conforme mostrado no exemplo a seguir para o **Excel4** e ** Excel12**.
  
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

Na prática, a função **Excel12v_example**, pode ser classificada com mais eficiência, criando um único argumento**xltypeMulti** **XLOPER12** e chamando a API C usando **Excel12**, conforme mostrado no exemplo a seguir.
  
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
> Nesse caso, o valor de retorno **Excel12** será ignorado. Em vez disso, o código verifica que o**XLOPER12** fornecido é **xltypeNum** para determinar se a chamada foi bem-sucedida. 
  
## <a name="xlcallver"></a>XLCallVer

Além dos retornos de chamada **Excel4**, **Excel4v**, **Excel12**, e **Excel12v**, o Excel exporta uma função ** XLCallVer**, que retorna a versão da API C em execução.
  
O protótipo da função é o seguinte:
  
 `int pascal XLCallVer(void);`
  
Você pode chamar essa função, que é thread-safe, de qualquer comando ou função XLL.
  
Do Excel 97 até o Excel 2003, **XLCallVer** retorna 0x0500 = 1280 hex = 5 x 256, que indica o Excel versão 5. A partir do Excel 2007, ela retorna 3072 = 0x0c00 hex = 12 x 256, que indica a versão 12 da mesma forma.
  
Embora você possa usar isso para determinar se a nova API de C está disponível em tempo de execução, talvez você prefira detectar a versão do Excel em execução usando `Excel4(xlfGetWorkspace, &version, 1, &arg)`, no qual `arg` é um numérico **XLOPER** definido para 2. A função retorna uma cadeia de caracteres **XLOPER**, versão, que pode ser forçada a um número inteiro. O motivo para confiar na versão do Excel em vez da versão da API C é que existem diferenças entre o Excel 2000, o Excel 2002 e o Excel 2003 que o seu suplemento também pode precisar detectar. Por exemplo, foram feitas alterações na precisão de algumas das funções estatísticas.
  
## <a name="see-also"></a>Confira também

- [Criar XLLs](creating-xlls.md)  
- [Acessar o código de XLL no Excel](accessing-xll-code-in-excel.md)  
- [Excel XLL SDK API Function Reference](excel-xll-sdk-api-function-reference.md)  
- [Retorno de chamada da API de C: funções Excel4, Excel12](c-api-callback-functions-excel4-excel12.md)  
- [Desenvolvimento de XLLs do Excel](developing-excel-xlls.md)

