---
title: Gerenciamento de memória no Excel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
keywords:
- memória XLOPER12 [Excel 2007], gerenciamento de memória no Excel, pilha do Excel, cadeias de caracteres [Excel 2007], gerenciamento de memória, gerenciamento de memória no Excel, memória XLOPER [Excel 2007], memória [Excel 2007], diretrizes de gerenciamento
localization_priority: Normal
ms.assetid: 3bf5195b-6235-43cf-8795-0c7b0a63a095
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: f129dac2971f01c8ada15f0028958132b1945746
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419538"
---
# <a name="memory-management-in-excel"></a>Gerenciamento de memória no Excel

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
O gerenciamento de memória é a preocupação mais importante se você quiser criar XLLs eficientes e estáveis. A falha no gerenciamento da memória pode levar a uma variedade de problemas no Microsoft Excel, desde pequenos problemas, como alocação de memória ineficiente e vazamentos de memória pequenos, para grandes problemas, como a desestabilização do Excel.
  
O gerenciamento inconsistente de memória é a fonte mais comum de problemas relacionados a suplementos sérios. Portanto, você deve criar seu projeto com uma estratégia consistente e bem elaborada sobre o gerenciamento de memória. 
  
O gerenciamento de memória ficou mais complexo no Microsoft Office Excel 2007 com a introdução do recálculo de pasta de trabalho multithread. Se você quiser criar e exportar funções de planilha com segurança de thread, você deve gerenciar os conflitos resultantes que podem ocorrer quando vários threads competem o acesso.
  
Há considerações de memória para os seguintes três tipos de estrutura de dados:
  
- **XLOPER**s e **XLOPER12**s
    
- Cadeias de caracteres que não estão em um **XLOPER** ou **XLOPER12**
    
- Matrizes de **FP** e **FP12** 
    
## <a name="xloperxloper12-memory"></a>Memória XLOPER/XLOPER12

A estrutura de dados **XLOPER**/ **XLOPER12** tem alguns subtipos que contêm ponteiros para blocos de memória, como cadeias de caracteres (**xltypeStr**), matrizes (**xltypeMulti**) e referências externas (**xltypeRef**). Observe também que as matrizes do **xltypeMulti** podem conter cadeias de caracteres ****/ de**XLOPER12s** que, por sua vez, apontam para outros blocos de memória. 
  
Um **XLOPER**/ **XLOPER12** pode ser criado de várias maneiras: 
  
- Pelo Excel ao preparar argumentos para serem passados para uma função XLL
    
- Pelo Excel ao retornar **XLOPER** ou **XLOPER12** em uma chamada da API C 
    
- Pela sua DLL ao criar argumentos a serem passados para uma chamada da API de C
    
- Por sua DLL ao criar um valor de retorno da função XLL
    
Um bloco de memória dentro de um dos tipos de apontador de memória pode ser alocado de várias maneiras:
  
- Pode ser um bloco estático dentro da sua DLL fora de qualquer código de função e, nesse caso, você não precisa alocar ou liberar a memória.
    
- Pode ser um bloco estático dentro da sua DLL dentro de algum código de função e, nesse caso, você não precisa alocar ou liberar a memória.
    
- Ela pode ser alocada dinamicamente e liberada por sua DLL de várias maneiras possíveis: **malloc** e **Free**, **New** e **delete**, e assim por diante.
    
- Ele pode ser alocado dinamicamente pelo Excel.
    
Dada a quantidade de possíveis origens para a memória **XLOPER**/ **XLOPER12** e o número de situações nas quais o **XLOPER**/ **XLOPER12** pode ter tido essa memória atribuída, não é surpresa que esse assunto possa Parece muito difícil. No enTanto, a complexidade pode ser muito reduzida se você seguir várias regras e diretrizes. 
  
### <a name="rules-for-working-with-xloperxloper12"></a>Regras para trabalhar com XLOPER/XLOPER12

- Não tente liberar memória ou substituir **XLOPER**/ **XLOPER12**s que são passados como argumentos para a função XLL. Você deve tratar esses argumentos como somente leitura. Para obter mais informações, consulte "retornando **XLOPER** ou **XLOPER12** modificando argumentos no local" em [problemas conhecidos no desenvolvimento XLL do Excel](known-issues-in-excel-xll-development.md).
    
- Se o Excel alocou memória para um **XLOPER**/ **XLOPER12** retornado para sua dll em uma chamada para a API de C: 
    
  - Você deve liberar a memória quando não precisar mais do **XLOPER**/ **XLOPER12** usando uma chamada a [xlFree](xlfree.md). Não use nenhum outro método, como livre ou excluído, para liberar a memória.
    
  - Se o tipo retornado for **xltypeMulti**, não substitua nenhum **XLOPER**/ **XLOPER12**s dentro da matriz, especialmente se eles contiverem cadeias de caracteres e, especialmente, onde você está tentando substituir por uma cadeia de caracteres.
    
  - Se você quiser retornar o **XLOPER**/ **XLOPER12** ao Excel como o valor de retorno da função DLL, deverá informar ao Excel que há memória que o Excel deve liberar quando tiver terminado. 
    
- Você só deve chamar **xlFree** em um **XLOPER**/ **XLOPER12** que foi criado como o valor de retorno para uma chamada da API de C. 
    
- Se sua dll alocou memória para um **XLOPER**/ **XLOPER12** que você deseja retornar ao Excel como o valor de retorno da função DLL, você deve informar ao Excel que há memória que a DLL deve liberar. 
    
### <a name="guidelines-for-memory-management"></a>Diretrizes para gerenciamento de memória

- Seja consistente em sua DLL no método que você usa para alocar e liberar memória. Evite misturar métodos. Uma boa abordagem é envolver o método que você está usando em uma classe de memória ou estrutura, dentro da qual você pode alterar o método usado sem alterar seu código em muitos lugares.
    
- Ao criar matrizes do **xltypeMulti** dentro da sua dll, seja consistente na forma como você aloca memória para cadeias de caracteres: sempre aloque dinamicamente a memória para elas ou sempre use a memória estática. Se você fizer isso, quando estiver liberando a memória, saberá que você deve sempre ou nunca liberar as cadeias de caracteres. 
    
- Faça cópias profundas da memória alocada no Excel quando você estiver copiando um ****/ **XLOPER12**XLOPER criado pelo Excel.
    
- Não coloque cadeias de caracteres de ****/ sequência de caracteres alocadas do Excel**XLOPER12**s dentro de matrizes do **xltypeMulti** . Faça cópias profundas das cadeias de caracteres e armazene ponteiros para as cópias na matriz. 
    
## <a name="freeing-excel-allocated-xloperxloper12-memory"></a>Liberando memória XLOPER/XLOPER12 alocada ao Excel

Considere o seguinte comando XLL, que usa **xlGetName** para obter uma cadeia de caracteres contendo o caminho e o nome de arquivo da dll e o exibe em uma caixa de diálogo de alerta usando o **xlcAlert**.
  
```cs
int WINAPI show_DLL_name(void)
{
    XLOPER12 xDllName;
    if(Excel12(xlfGetName, &xDllName, 0) == xlretSuccess)
    {
        // Display the name.
        Excel12(xlcAlert, 0, 1, &xDllName);
        // Free the memory that Excel allocated for the string.
        Excel12(xlFree, 0, 1, &xDllName);
    }
    return 1;
}

```

Quando a função não precisa mais da memória apontada pelo **xDllName**, ela pode liberá-la usando uma chamada para a [função xlFree](xlfree.md), uma das funções da API C-only da dll. 
  
A função **xlFree** está totalmente documentada na seção de referência de função (consulte [funções da API C que podem ser chamadas apenas de uma DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)), mas lembre-se do seguinte:
  
- você pode passar ponteiros para mais de um **XLOPER**/ **XLOPER12**s em uma única chamada para **xlFree**, limitado apenas pelo número de argumentos de função com suporte na versão em execução do excel (30 no excel 2003, 255 a partir do excel 2007).
    
- **xlFree** define o ponteiro contido como **nulo** para garantir que uma tentativa de liberar um ****/ **XLOPER12** XLOPER que já tenha sido liberado é segura. **xlFree** é a única função da API C que modifica seus argumentos. 
    
- Você pode chamar o **xlFree** com segurança em qualquer**XLOPER12** **XLOPER**/ usado para o valor de retorno de uma chamada para a API de C, independentemente se ele contém um ponteiro para a memória. 
    
## <a name="returning-xloperxloper12s-to-be-freed-by-excel"></a>Retornar XLOPER/XLOPER12s a ser liberado pelo Excel

Suponha que você quisesse modificar o comando de exemplo na seção anterior e alterá-lo para uma função de planilha que retorna o caminho de DLL e o nome do arquivo quando passado um argumento **true** **Boolean** e **#N/a** caso contrário. Sem dúvida, não é possível chamar **xlFree** para liberar a memória da cadeia de caracteres antes de devolvê-la ao Excel. No enTanto, se não for liberado em algum momento, o suplemento vazará memória toda vez que a função for chamada. Para contornar esse problema, você pode definir um bit no campo **xltype** do **XLOPER**/ **XLOPER12**, definido como **xlbitXLFree** em xlcall. h. Definir isso informa ao Excel que ele deve liberar a memória retornada quando terminar de copiar o valor. 
  
### <a name="example"></a>Exemplo

O exemplo de código a seguir mostra o comando XLL da seção anterior convertida em uma função de planilha XLL.
  
```cs
LPXLOPER12 WINAPI get_DLL_name(int calculation_trigger)
{
    static XLOPER12 xRtnValue; // Not thread-safe
    Excel12(xlfGetName, &xRtnValue, 0);
// If xlfGetName failed, xRtnValue will be #VALUE!
    if(xRtnValue.xltype == xltypeStr)
    {
// Tell Excel to free the string memory after
// it has copied out the return value.
        xRtnValue.xltype |= xlbitXLFree;
    }
    return &xRtnValue;
}
```

Funções XLL que usam **XLOPER**/ **XLOPER12**s devem ser declaradas como pegar e retornar ponteiros para **XLOPER**/ **XLOPER12**s. O uso neste exemplo de um **XLOPER12** estático dentro da função não é thread-safe. Você pode registrar incorretamente essa função como thread-safe, mas o risco **xRtnValue** ser substituído por um thread antes que outro thread tivesse concluído. 
  
Você deve definir **xlbitXLFree** após a chamada para o retorno de chamada do Excel que o aloca. Se você defini-la antes disso, ela será sobrescrita e não terá o efeito desejado. Se você pretende usar o valor como um argumento em uma chamada para outra função da API C antes de devolvê-lo à planilha, você deve definir esse bit após qualquer chamada. Caso contrário, você confundirá funções que não mascaram esse bit antes de verificar o tipo de**XLLOPER12** **XLOPER**/ . 
  
## <a name="returning-xloperxloper12s-to-be-freed-by-the-dll"></a>Retornar XLOPER/XLOPER12s a ser liberado pela DLL

Um problema semelhante a isso ocorre quando seu XLL alocou memória para um **XLOPER**/ **XLOPER12** e deseja retorná-lo ao Excel. O Excel reconhece outro bit que pode ser definido no campo **xltype** do **XLOPER**/ **XLOPER12**, definido como **xlbitDLLFree** em xlcall. h. 
  
Quando o Excel recebe **um XLOPER**/ **XLOPER12** com esse conjunto de bits, ele tenta chamar uma função que deve ser exportada pelo XLL chamado [xlAutoFree](xlautofree-xlautofree12.md) (para **XLOPER**s) ou **xlAutoFree12** (para **XLOPER12**s). Essa função é descrita mais completamente na referência de função (consulte [Gerenciador de suplementos e funções da interface XLL](add-in-manager-and-xll-interface-functions.md)), mas um exemplo de implementação mínima é fornecido aqui. Sua finalidade é liberar a memória **XLOPER**/ **XLOPER12** de forma consistente com a forma como ela foi alocada originalmente. 
  
### <a name="examples"></a>Exemplos

A função de exemplo a seguir faz o mesmo que a função anterior, exceto pelo fato de que ela inclui o texto "o nome de caminho completo para esta DLL é" antes do nome da DLL.
  
```cs
#include <string.h>
LPXLOPER12 WINAPI get_DLL_name_2(int calculation_trigger)
{
    static XLOPER12 xRtnValue; // Not thread-safe
    Excel12(xlfGetName, &xRtnValue, 0);
// If xlfGetName failed, xRtnValue will be #VALUE!
    if(xRtnValue.xltype != xltypeStr)
        return &xRtnValue;
// Make a copy of the DLL path and file name.
    wchar_t *leader = L"The full pathname for this DLL is ";
    size_t leader_len = wcslen(leader);
    size_t dllname_len = xRtnValue.val.str[0];
    size_t msg_len = leader_len + dllname_len;
    wchar_t *msg_text = (wchar_t *)malloc(msg_len + 1);
    wcsncpy_s(msg_text + 1, leader, leader_len);
    wcsncpy_s(msg_text + 1 + leader_len, xRtnValue.val.str + 1,
        dllname_len);
    msg_text[0] = msg_len;
// Now the original string has been copied Excel can free it.
    Excel12(xlFree, 0, 1, &xRtnValue);
// Now reuse the XLOPER12 for the new string.
    xRtnValue.val.str = msg_text;
// Tell Excel to call back into the DLL to free the string
// memory after it has copied out the return value.
    xRtnValue.xltype     = xltypeStr | xlbitDLLFree;
    return &xRtnValue;
}
```

Uma implementação minimamente suficiente de **xlAutoFree12** no XLL que exportou a função anterior seria como a seguir. 
  
```cs
void WINAPI xlAutoFree12(LPXLOPER12 p_oper)
{
    if(p_oper->xltype == (xltypeStr | xlbitDLLFree))
        free(p_oper->val.str);
}
```

Essa implementação só será suficiente se o XLL retornar apenas cadeias de caracteres **XLOPER12** , e essas cadeias de caracteres serão alocadas apenas usando **malloc**. Observe que o teste 
  
 ` if(p_oper->xltype == xltypeStr) `
  
falhará nesse caso porque o **xlbitDLLFree** está definido. 
  
Em geral, **xlAutoFree** e **xlAutoFree12** devem ser implementados para que eles liberem memória associada a matrizES **xltypeMulti** criadas por XLL e as referências externas do **xltypeRef** . 
  
Você pode decidir implementar suas funções XLL para que todas elas retornem **XLOPER**s e **XLOPER12**s alocados dinamicamente. Nesse caso, você precisaria definir **xlbitDLLFree** em todos esses **XLOPER**s e **XLOPER12**s independentemente do subtipo. Você também precisaria implementar o **xlAutoFree** e o **xlAutoFree12** para que essa memória seja liberada e também qualquer memória apontada dentro do **XLOPER**/ **XLOPER12**. Essa abordagem é uma maneira de tornar o valor de retorno em thread seguro. Por exemplo, a função Previous pode ser reescrita da seguinte maneira.
  
```cs
#include <string.h>
LPXLOPER12 WINAPI get_DLL_name_3(int calculation_trigger)
{
// Thread-safe
    LPXLOPER12 pxRtnValue = (LPXLOPER12)malloc(sizeof(XLOPER12));
    Excel12(xlfGetName, pxRtnValue, 0);
// If xlfGetName failed, pxRtnValue will be #VALUE!
    if(pxRtnValue->xltype != xltypeStr)
    {
// Even though an error type does not point to memory,
// Excel needs to pass this oper to xlAutoFree12 to
// free pxRtnValue itself.
        pxRtnValue->xltype |= xlbitDLLFree;
        return pxRtnValue;
    }
// Make a copy of the DLL path and file name.
    wchar_t *leader = L"The full pathname for this DLL is ";
    size_t leader_len = wcslen(leader);
    size_t dllname_len = pxRtnValue->val.str[0];
    size_t msg_len = leader_len + dllname_len;
    wchar_t *msg_text = (wchar_t *)malloc(msg_len + 1);
    wcsncpy_s(msg_text + 1, leader, leader_len);
    wcsncpy_s(msg_text + 1 + leader_len, pxRtnValue->val.str + 1,
        dllname_len);
    msg_text[0] = msg_len;
// Now the original string has been copied Excel can free it.
    Excel12(xlFree, 0, 1, pxRtnValue);
// Now reuse the XLOPER12 for the new string.
    pxRtnValue->val.str = msg_text;
    pxRtnValue->xltype = xltypeStr | xlbitDLLFree;
    return pxRtnValue;
}
void WINAPI xlAutoFree12(LPXLOPER12 p_oper)
{
    if(p_oper->xltype == (xltypeStr | xlbitDLLFree))
        free(p_oper->val.str);
    free(p_oper);
}
```

Para obter mais informações sobre o **xlAutoFree** e o **XlAutoFree12**, consulte [xlAutoFree/xlAutoFree12](xlautofree-xlautofree12.md).
  
## <a name="returning-modify-in-place-arguments"></a>Retornando argumentos de modificação no local

O Excel permite que uma função XLL retorne um valor modificando um argumento no local. Só é possível fazer isso com um argumento passado como um ponteiro. Para funcionar dessa forma, a função deve ser registrada de uma maneira que informa ao Excel qual argumento será modificado. 
  
Esse método de retorno de um valor é suportado para todos os tipos de dados que podem ser passados por ponteiro, mas é especialmente útil para os seguintes tipos:
  
- Sequências de bytes ASCII de tamanho contado e terminada por caractere nulo
    
- Cadeias de caracteres largos Unicode de tamanho contado e terminada em nulo (começando no Excel 2007)
    
- Matrizes de ponto flutuante de **FP** 
    
- **FP12** matrizes de ponto flutuante (começando no Excel 2007) 
    
> [!NOTE]
> Você não deve tentar retornar **XLOPER**s ou **XLOPER12**s dessa maneira. Confira mais informações em [Problemas conhecidos no desenvolvimento de XLL do Excel](known-issues-in-excel-xll-development.md). 
  
A vantagem de usar essa técnica, em vez de apenas usar a instrução return, é que o Excel aloca a memória para os valores de retorno. Depois que o Excel concluir a leitura dos dados retornados, ele liberará a memória. Isso leva as tarefas de gerenciamento de memória para longe da função XLL. Essa técnica é thread-safe: se chamado simultaneamente pelo Excel em threads diferentes, cada chamada de função em cada thread tem seu próprio buffer.
  
É útil para os tipos de dados listados anteriormente, em particular, porque o mecanismo de chamada de retorno para a dll para liberar a memória post-return existente para **XLOPER**/ **XLOPER12**s não existe para cadeias de caracteres simples e **FP** /  Matrizes do **FP12** . Portanto, ao retornar uma cadeia de caracteres criada por DLL ou uma matriz de ponto flutuante, você tem as seguintes opções: 
  
- Definir um ponteiro persistente para um buffer alocado dinamicamente, retornar o ponteiro. Na próxima chamada para a função (1) Verifique se o ponteiro não é nulo, (2) libere os recursos alocados na chamada anterior e redefina o ponteiro como nulo, (3) reutilize o ponteiro de um bloco de memória recentemente alocado.
    
- Crie suas cadeias de caracteres e matrizes em um buffer estático que não precise ser liberado e retorne um ponteiro para isso.
    
- Modificar um argumento no lugar, gravando a cadeia de caracteres ou matriz diretamente no conjunto de espaços do Excel.
    
Caso contrário, você deve criar um **XLOPER**/ **XLOPER12**e usar **xlbitDLLFree** e **xlAutoFree**/ **xlAutoFree12** para liberar os recursos. 
  
A última opção pode ser a mais simples nesses casos em que você está sendo passado um argumento do mesmo tipo que o valor de retorno. O ponto-chave a ser lembrado é que os tamanhos de buffer são limitados e você deve ter muito cuidado para não satura-los. É possível que esse problema falhe no Excel. Tamanhos de buffer para cadeias de caracteres e**FP12** de **FP**/ são abordados a seguir. 
  
## <a name="strings"></a>Cadeias de caracteres

Problemas com o gerenciamento da memória da cadeia de caracteres são, supostamente, a causa mais comum de instabilidade em aplicativos e suplementos. É possível que seja compreensível, uma vez que as várias maneiras nas quais as cadeias de caracteres são tratadas: terminadas por caractere nulo ou de tamanho contado (ou ambos); buffers estáticos ou dinâmicos; comprimento fixo ou comprimento quase ilimitado; memória gerenciada do sistema operacional (por exemplo, OLE BSTR) ou cadeias de caracteres não gerenciadas; e assim por diante.
  
Os programadores de C/C++ estão mais familiarizados com cadeias de caracteres terminadas por caractere nulo. A biblioteca C padrão foi projetada para trabalhar com essas cadeias de caracteres. Literais de cadeia de caracteres estática no código são compilados em cadeias de caracteres terminadas em nulo. Como alternativa, o Excel funciona com cadeias de caracteres de tamanho contado que não estão em um término geral nulo. A combinação desses fatos requer uma abordagem clara e consistente em sua DLL/XLL em relação à forma como você lida com cadeias de caracteres e memória de cadeia de caracteres.
  
Os problemas mais comuns são os seguintes:
  
- A passagem de um ponteiro nulo ou inválido para uma função que espera um ponteiro válido e não ou não pode verificar a própria validade do ponteiro.
    
- A superexecução dos limites de um buffer de cadeia de caracteres por uma função que não ou não pode verificar o tamanho do buffer em relação ao comprimento da cadeia de caracteres que está sendo gravada.
    
- Tentar liberar a memória do buffer de cadeia de caracteres que é estática, ou já foi liberada, ou não foi alocada de uma maneira consistente com o modo como está sendo liberada.
    
- Vazamentos de memória que resultam de cadeias de caracteres sendo alocadas e, em seguida, não liberadas, geralmente em uma função chamada freqüentemente.
    
### <a name="rules-for-strings"></a>Regras para cadeias de caracteres

Assim como ****/ com o XLOPER**XLOPER**s, há regras e diretrizes que você deve seguir. As diretrizes são as mesmas que foram fornecidas na seção anterior. As regras aqui são uma extensão das regras especificamente para cadeias de caracteres.
  
 **Regras**
  
- Não tente liberar memória ou substituir as cadeias ****/ de caracteres de tamanho de cadeia de caracteres**XLOPER12**s ou de comprimento simples ou nulos passados como argumentos para a função XLL. Você deve tratar esses argumentos como somente leitura.
    
- Onde o Excel aloca memória para um **XLOPER**/ de cadeia de caracteres**XLOPER12** para o valor de retorno de uma função de retorno de chamada de API de C, use **xlFree** para liberá-lo ou defina **xlbitXLFree** se retornar ao Excel a partir de uma função XLL. 
    
- Onde sua dll aloca dinamicamente um buffer de cadeia de caracteres para um **XLOPER**/ **XLOPER12**, liberá-lo de forma consistente com a forma como você o alocou quando tiver terminado, ou definir **xlbitDLLFree** se retornar ao Excel a partir de uma função XLL e liberá-lo em **xlAutoFree** /  **xlAutoFree12**.
    
- Se o Excel alocou memória para uma matriz **xltypeMulti** retornada à sua dll em uma chamada para a API de C, não substitua nenhum **XLOPER**/ de cadeia de caracteres**XLOPER12**s dentro da matriz. Essas matrizes só devem ser liberadas usando **xlFree**ou, se forem retornadas por uma função XLL, definindo **xlbitXLFree**.
    
### <a name="string-types-supported"></a>Tipos de cadeia de caracteres suportados

**XltypeStr de API C/XLOPER12s**

|* * Cadeias de caracteres de byte: * * XLOPER * * * *|* * Cadeias de caracteres largos: * * XLOPER12 * * * *|
|:-----|:-----|
|Todas as versões do Excel  <br/> |Iniciando no Excel 2007  <br/> |
|Comprimento máximo: 255 bytes estendidos ASCII  <br/> |Caracteres Unicode de comprimento máximo 32.767  <br/> |
|Byte primeiro (não assinado) = comprimento  <br/> |Primeiro caractere Unicode = comprimento  <br/> |
   
> [!IMPORTANT]
> Não assuma a terminação nula de cadeias de caracteres **XLOPER** ou **XLOPER12** . 
  
**Cadeias de caracteres C/C++**

|**Cadeias de caracteres de byte**|**Cadeias de caracteres largos**|
|:-----|:-----|
|Terminada em nulo (**Char** *) "C" tamanho máximo: 255 bytes ASCII estendidos  <br/> |Terminada em nulo (**wchar_t** *) "C%" tamanho máximo de 32.767 caracteres Unicode  <br/> |
|Comprimento contado (unsigned**Char** *) "D"  <br/> |Comprimento contado (**wchar_t** *) "D%"  <br/> |
   
### <a name="strings-in-xltypemulti-xloperxloper12-arrays"></a>Cadeias de caracteres em matrizes xltypeMulti XLOPER/XLOPER12

Em vários casos, o Excel cria uma matriz **xltypeMulti** para uso em sua dll/XLL. Várias das funções de informações XLM retornam essas matrizes. Por exemplo, a função da API C **xlfGetWorkspace**, quando passado o argumento *44* , retorna uma matriz contendo cadeias de caracteres que DESCREVEM todos os procedimentos dll registrados no momento. A função da API C **xlfDialogBox** retorna uma cópia modificada do seu argumento de matriz, contendo cópias profundas das cadeias de caracteres. Talvez a maneira mais comum de que um XLL encontre uma matriz **xltypeMulti** seja onde ela foi passada como um argumento para uma função XLL ou foi forçada a esse tipo de uma referência de intervalo. Nesses últimos casos, o Excel cria cópias profundas das cadeias de caracteres nas células de origem e aponta para elas dentro da matriz. 
  
Onde você deseja modificar essas cadeias de caracteres em sua DLL, você deve fazer suas próprias cópias profundas. Ao criar suas próprias matrizes do **xltypeMulti** , você não deve colocar a cadeia de caracteres ****/ ****. Esses riscos não são liberados corretamente mais tarde ou não os liberam. Novamente, você deve fazer cópias profundas das cadeias de caracteres e armazenar ponteiros para as cópias na matriz.
  
 **Exemplos**
  
A função de exemplo a seguir cria uma cópia alocada dinamicamente de uma cadeia de caracteres Unicode contada por comprimento. Observe que o chamador deve liberar a memória alocada neste exemplo usando **delete**[], e que a cadeia de caracteres de origem não é considerada nula terminada. A cadeia de caracteres de cópia será truncada se necessário para segurança e não será terminada em nulo.
  
```cs
#include <string.h>
#define MAX_V12_STRBUFFLEN    32678
    
wchar_t * deep_copy_wcs(const wchar_t *p_source)
{
    if(!p_source)
        return NULL;
    size_t source_len = p_source[0];
    bool truncated = false;
    if(source_len >= MAX_V12_STRBUFFLEN)
    {
        source_len = MAX_V12_STRBUFFLEN - 1; // Truncate the copy
        truncated = true;
    }
    wchar_t *p_copy = new wchar_t[source_len + 1];
    wcsncpy_s(p_copy, p_source, source_len + 1);
    if(truncated)
        p_copy[0] = source_len;
    return p_copy;
}
```

Essa função pode ser usada com segurança para copiar um **XLOPER12**, conforme mostrado na seguinte função exportável XLL que retorna uma cópia do seu argumento se for uma cadeia de caracteres. Todos os outros tipos são retornados como uma cadeia de comprimento zero. Observe que os intervalos não são tratados, a função retorna **#VALUE!**. A função deve ser registrada como pegar um argumento de tipo U para que as referências sejam passadas como valores. Isso equivale à função de planilha interna **T ()** , exceto pelo fato de **** que astext também converte erros em cadeias de caracteres de comprimento zero. Este exemplo de código pressupõe que o **xlAutoFree12** libera o ponteiro passado, e também seu conteúdo, usando **delete**.
  
```cs
LPXLOPER12 WINAPI AsText(LPXLOPER12 pArg)
{
    LPXLOPER12 pRtnVal = new XLOPER12;
// If the input was an array, only operate on the top-left element.
    LPXLOPER *pTemp;
    if(pArg->xltype == xltypeMulti)
        pTemp = pArg->val.array.lparray;
    else
        pTemp = pArg;
    switch(pTemp->xltype)
    {
        case xltypeErr:
        case xltypeNum:
        case xltypeMissing:
        case xltypeNil:
        case xltypeBool:
            pRtnVal->xltype = xltypeStr | xlbitDLLFree;
            pRtnVal->val.str = deep_copy_wcs(L"\000");
            return pRtnVal;
        case xltypeStr:
            pRtnVal->xltype = xltypeStr | xlbitDLLFree;
            pRtnVal->val.str = deep_copy_wcs(pTemp->val.str);
            return pRtnVal;
        
        default: // xltypeSRef, xltypeRef, xltypeFlow, xltypeInt
            pRtnVal->xltype = xltypeErr | xlbitDLLFree;
            pRtnVal->val.err = xlerrValue;
            return pRtnVal;
    }
}
```

### <a name="returning-modify-in-place-string-arguments"></a>Retornando argumentos de cadeia de caracteres de modificação no local

Argumentos registrados como Types **F**, **G**, **F%** e **G%** podem ser modificados no local. Quando o Excel está preparando argumentos de cadeia de caracteres para esses tipos, ele cria um buffer de comprimento máximo. Em seguida, ele copia a cadeia de caracteres de argumento para isso, mesmo que essa cadeia de caracteres seja muito mais curta. Isso permite que a função XLL escreva o valor de retorno diretamente na mesma memória. 
  
Os tamanhos de buffer definidos para esses tipos são os seguintes:
  
- **Cadeias de caracteres de byte:** 256 bytes incluindo o contador de comprimento (tipo G) ou de finalização nula (tipo F). 
    
- Cadeias de caracteres **Unicode:** 32.768 caracteres largos (65.536 bytes) incluindo o contador comprimento (tipo G%) ou de finalização nula (tipo F%). 
    
> [!NOTE]
> Não é possível chamar essa função diretamente do Visual Basic for Applications (VBA) porque você não pode garantir que um buffer suficientemente grande tenha sido alocado. Você só pode chamar essa função de outra DLL com segurança se tiver passado explicitamente um buffer suficientemente grande. 
  
Veja a seguir um exemplo de uma função XLL que reverte uma cadeia de caracteres largo terminada por nulo usando a função de biblioteca padrão **wcsrev**. O argumento nesse caso seria registrado como o tipo **F%**.
  
```cs
void WINAPI reverse_text_xl12(wchar_t *text)
{
    _wcsrev(text);
}
```

## <a name="persistent-storage-binary-names"></a>Armazenamento persistente (nomes binários)

Os nomes binários são definidos e associados aos blocos de binários, ou seja, não estruturados, que são armazenados juntos com a pasta de trabalho. Eles são criados usando a função [xlDefineBinaryName](xldefinebinaryname.md)e os dados são recuperados usando a função [xlGetBinaryName](xlgetbinaryname.md). Ambas as funções são descritas em mais detalhes na referência de função (consulte [funções da API de C que podem ser chamadas apenas de uma DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)) e ambos usam o **xltypeBigData** **XLOPER**/ **XLOPER12**. 
  
Para obter informações sobre problemas conhecidos que limitam os aplicativos práticos de nomes binários, consulte [problemas conhecidos no desenvolvimento de XLL do Excel](known-issues-in-excel-xll-development.md).
  
## <a name="excel-stack"></a>Pilha do Excel

O Excel compartilha o espaço em pilha com todas as DLLs carregadas. O espaço de pilha geralmente é mais do que adequado para uso comum, e você não precisa se preocupar com ele desde que siga algumas diretrizes: 
  
- Não transmita estruturas muito grandes como argumentos para funções por valor na pilha. Passe em vez de ponteiros ou referências.
    
- Não retorna estruturas grandes na pilha. Retornar ponteiros para memória estática ou dinamicamente alocada ou usar argumentos passados por referência.
    
- Não declare estruturas de variáveis automáticas muito grandes no código de função. Se você precisar deles, declare-os como estáticos.
    
- Não chame funções recursivamente, a menos que você tenha certeza de que a profundidade da recursão sempre será superficial. Em vez disso, tente usar um loop.
    
Quando uma DLL chama de volta para o Excel usando a API C, o Excel verifica primeiro se há espaço suficiente na pilha para a chamada de uso de pior caso que pudesse ser feita. Se ele achar que pode haver espaço insuficiente, a chamada será malsucedida, mesmo que possa ter espaço suficiente para essa chamada específica. Nesse caso, os retornos de chamada retornam o código **xlretFailed**. Para uso comum da API C e da pilha, isso é uma improvável causa da falha de uma chamada da API de C.
  
Se estiver preocupado, ou apenas curioso, ou se quiser eliminar falta de espaço de pilha como motivo para uma falha não explicada, você pode descobrir quanto espaço de pilha há com uma chamada para a função [xlStack](xlstack.md) . 
  
## <a name="see-also"></a>Confira também



[Recálculo com vários threads no Excel](multithreaded-recalculation-in-excel.md)
  
[Multithreading e conTenção de memória no Excel](multithreading-and-memory-contention-in-excel.md)
  
[Desenvolvimento de XLLs do Excel](developing-excel-xlls.md)

