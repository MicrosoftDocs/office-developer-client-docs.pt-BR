---
title: Gerenciamento de Memória no Excel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
keywords:
- xloper12 memory [excel 2007],managing memory in Excel,Excel stack,strings [Excel 2007], managing memory,memory management in Excel,XLOPER memory [Excel 2007],memory [Excel 2007], management guidelines
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
# <a name="memory-management-in-excel"></a>Gerenciamento de Memória no Excel

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
O gerenciamento de memória é a preocupação mais importante se você quiser criar XLLs eficientes e estáveis. A falha ao gerenciar bem a memória pode levar a uma variedade de problemas no Microsoft Excel— desde pequenos problemas, como alocação e inicialização ineficientes de memória e pequenos vazamentos de memória, até problemas importantes, como a desestabilização do Excel.
  
O erro de gestão da memória é a fonte mais comum de problemas sérios relacionados a complementos. Portanto, você deve criar seu projeto com uma estratégia consistente e bem pensada no gerenciamento de memória. 
  
O gerenciamento de memória tornou-se mais complexo no Microsoft Office Excel 2007 com a introdução do recálculo de várias planilhas. Se você quiser criar e exportar funções de planilha thread-safe, gerencie os conflitos resultantes que podem ocorrer quando vários threads competem pelo acesso.
  
Há considerações de memória para os três tipos de estrutura de dados a seguir:
  
- **XLOPER** s e **XLOPER12** s
    
- Cadeias de caracteres que não estão em **um XLOPER** ou **XLOPER12**
    
- **Matrizes FP** e **FP12** 
    
## <a name="xloperxloper12-memory"></a>Memória XLOPER/XLOPER12

A estrutura de dados **XLOPER** XLOPER12 tem alguns subtipos que contêm ponteiros para blocos de memória, ou /   seja, cadeias de caracteres (**xltypeStr**), matrizes (**xltypeMulti**) e referências externas (**xltypeRef**). Observe também que **matrizes xltypeMulti** podem conter cadeia de caracteres **XLOPER XLOPER12s** que, por sua vez, apontam /   para outros blocos de memória. 
  
Um **XLOPER** /  **XLOPER12** pode ser criado de várias maneiras: 
  
- Pelo Excel ao preparar argumentos para serem passados para uma função XLL
    
- By Excel when returning an **XLOPER** or **XLOPER12** in a C API call 
    
- Pela sua DLL ao criar argumentos a serem passados para uma chamada da API C
    
- Por sua DLL ao criar um valor de retorno de função XLL
    
Um bloco de memória em um dos tipos apontando para memória pode ser alocado de várias maneiras:
  
- Pode ser um bloco estático dentro de sua DLL fora de qualquer código de função, caso em que você não precisa alocar ou liberar a memória.
    
- Ele pode ser um bloco estático dentro de sua DLL dentro de algum código de função, caso em que você não precisa alocar ou liberar a memória.
    
- Ele pode ser alocado dinamicamente e liberado por sua DLL  de várias maneiras possíveis: **mallocal,** **gratuito,** novo e **excluído,** e assim por diante.
    
- Ele pode ser alocado dinamicamente pelo Excel.
    
Dado o número de origens possíveis para a memória /  **XLOPER XLOPER12** e o número de situações em que o **XLOPER** /  **XLOPER12** pode ter essa memória atribuída, não é surpreendente que esse assunto possa parecer muito difícil. No entanto, a complexidade poderá ser bastante reduzida se você seguir várias regras e diretrizes. 
  
### <a name="rules-for-working-with-xloperxloper12"></a>Regras para trabalhar com XLOPER/XLOPER12

- Não tente liberar memória ou substituir **XLOPERs** /  **XLOPER12** s que são passados como argumentos para sua função XLL. Você deve tratar esses argumentos como somente leitura. Para obter mais informações, consulte "Retornando **XLOPER** ou **XLOPER12** modificando argumentos no local" em Problemas conhecidos no desenvolvimento [de XLL do Excel.](known-issues-in-excel-xll-development.md)
    
- Se o Excel tiver alocado memória para um /  **XLOPER XLOPER12 retornado** à sua DLL em uma chamada para a API de C: 
    
  - Você deve liberar a memória quando não precisar mais do **XLOPER** /  **XLOPER12** usando uma chamada para [xlFree](xlfree.md). Não use qualquer outro método, como gratuito ou excluído, para liberar a memória.
    
  - Se o tipo retornado for **xltypeMulti**, não sobrescreva **nenhum** /  **XLOPER XLOPER12** s dentro da matriz, especialmente se eles contêm cadeias de caracteres e, especialmente, não onde você está tentando substituir com uma cadeia de caracteres.
    
  - Se quiser retornar o **XLOPER XLOPER12** para o Excel como o valor de retorno da função DLL, você deve dizer ao Excel que há memória que o Excel deve liberar quando /   terminar. 
    
- Você só deve chamar **xlFree** em um  /  **XLOPER XLOPER12** que foi criado como o valor de retorno para uma chamada de API C. 
    
- Se sua DLL alocou memória para um /  **XLOPER XLOPER12** que você deseja retornar ao Excel como o valor de retorno da função DLL, você deve dizer ao Excel que há memória que a DLL deve liberar. 
    
### <a name="guidelines-for-memory-management"></a>Diretrizes para gerenciamento de memória

- Seja consistente em sua DLL no método que você usa para alocar e liberar memória. Evite misturar métodos. Uma boa abordagem é quebrar o método que você está usando em uma classe ou estrutura de memória, dentro da qual você pode alterar o método usado sem alterar seu código em muitos lugares.
    
- Ao criar matrizes **xltypeMulti** em sua DLL, seja consistente na maneira como aloca memória para cadeias de caracteres: sempre aloce dinamicamente a memória para elas ou sempre use memória estática. Se você fizer isso, quando estiver liberando a memória, você vai saber que deve sempre ou nunca liberar as cadeias de caracteres. 
    
- Faça cópias profundas da memória alocada pelo Excel quando estiver copiando um **XLOPER** /  **XLOPER12** criado pelo Excel.
    
- Não coloque a cadeia de caracteres **alocada** do Excel /  **XLOPER XLOPER12** s em **matrizes xltypeMulti.** Faça cópias profundas das cadeias de caracteres e armazene ponteiros para as cópias na matriz. 
    
## <a name="freeing-excel-allocated-xloperxloper12-memory"></a>Liberando Excel-Allocated memória XLOPER/XLOPER12

Considere o seguinte comando XLL, que usa **xlGetName** para obter uma cadeia de caracteres contendo o caminho e o nome de arquivo da DLL e exibe-o em uma caixa de diálogo de alerta usando **xlcAlert**.
  
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

Quando a função não precisa mais da memória apontada por **xDllName**, ela pode libera-la usando uma chamada para a função [xlFree](xlfree.md), uma das funções da API C somente DLL. 
  
A **função xlFree** está totalmente documentada na seção de referência de função (consulte Funções da API C que podem ser chamadas apenas de uma DLL ou [XLL),](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)mas esteja ciente do seguinte:
  
- Você pode passar ponteiros para mais de um **XLOPER** XLOPER12 s em uma única chamada para xlFree , limitado somente pelo número de argumentos de função com suporte na versão em execução do /  Excel (30 no Excel 2003, 255 a partir do Excel 2007). 
    
- **XlFree** define o ponteiro contido como **NULL** para garantir que uma tentativa de liberar um  /  **XLOPER XLOPER12** que já foi liberado seja segura. **XlFree** é a única função da API C que modifica seus argumentos. 
    
- Você pode chamar **xlFree** com segurança em qualquer  /  **XLOPER XLOPER12 usado** para o valor de retorno de uma chamada para a API de C, independentemente de ele conter um ponteiro para a memória. 
    
## <a name="returning-xloperxloper12s-to-be-freed-by-excel"></a>Retornar XLOPER/XLOPER12s a ser liberado pelo Excel

Suponha que você quisesse modificar o comando de exemplo na seção anterior e alterá-lo para uma função de planilha que retorna o caminho DLL e o nome de arquivo quando passado um argumento **booliana** **verdadeiro** e **#N/A** caso contrário. Claramente, você não pode chamar **xlFree** para liberar a memória da cadeia de caracteres antes de reconselhá-la para o Excel. No entanto, se ele não for liberado em algum momento, o complemento irá liberar memória sempre que a função for chamada. Para resolver esse problema, você pode definir um pouco no campo **xltype** do  /  **XLOPER XLOPER12**, definido como **xlbitXLFree** em xlcall.h. Definir isso informa ao Excel que ele deve liberar a memória retornada quando terminar de copiar o valor. 
  
### <a name="example"></a>Exemplo

O exemplo de código a seguir mostra o comando XLL na seção anterior convertida em uma função de planilha XLL.
  
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

As funções XLL que usam **XLOPER** XLOPER12 s devem ser declaradas como utilizando e retornando ponteiros para /    /  **XLOPER XLOPER12** s. O uso neste exemplo de um **XLOPER12 estático** dentro da função não é thread-safe. Você poderia registrar incorretamente essa função como thread-safe, mas poderia correr o risco de **xRtnValue** ser substituído por um thread antes que outro thread tivesse terminado com ele. 
  
Você deve definir **xlbitXLFree após** a chamada para o retorno de chamada do Excel que a aloca. Se você defini-lo antes disso, ele será substituído e não terá o efeito desejado. Se você pretende usar o valor como um argumento em uma chamada para outra função da API C antes de revolvê-lo à planilha, deverão definir esse bit após qualquer chamada. Caso contrário, você confundirá funções que não mascaram esse bit antes de verificar o tipo /  **XLOPER XLLOPER12.** 
  
## <a name="returning-xloperxloper12s-to-be-freed-by-the-dll"></a>Retornar XLOPER/XLOPER12s a ser liberado pela DLL

Um problema semelhante a isso ocorre quando o XLL alocou memória para um  /  **XLOPER XLOPER12** e deseja devolvê-la para o Excel. O Excel reconhece outro bit que pode ser definido no campo **xltype** do **XLOPER** /  **XLOPER12**, definido como **xlbitDLLFree** em xlcall.h. 
  
Quando o Excel recebe um **XLOPER** XLOPER12 com este conjunto de bits, ele tenta chamar uma função que deve ser exportada pelo XLL chamado /   [xlAutoFree](xlautofree-xlautofree12.md) (para **XLOPER** s) ou **xlAutoFree12** (para **XLOPER12** s). Esta função é descrita com mais detalhes na referência de função (consulte o Gerenciador de Complementos e funções de [interface XLL),](add-in-manager-and-xll-interface-functions.md)mas um exemplo de implementação mínima é dado aqui. Seu objetivo é liberar a memória /  **XLOPER XLOPER12** de maneira consistente com a forma como foi originalmente alocada. 
  
### <a name="examples"></a>Exemplos

A função de exemplo a seguir faz o mesmo que a função anterior, exceto por incluir o texto "The full pathname for this DLL is " antes do nome da DLL.
  
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

Uma implementação minimamente suficiente de **xlAutoFree12** na XLL que exportou a função anterior seria a seguinte. 
  
```cs
void WINAPI xlAutoFree12(LPXLOPER12 p_oper)
{
    if(p_oper->xltype == (xltypeStr | xlbitDLLFree))
        free(p_oper->val.str);
}
```

Essa implementação só será suficiente se o XLL retornar somente cadeias de caracteres **XLOPER12** e essas cadeias de caracteres só são alocadas usando **malloc**. Observe que o teste 
  
 ` if(p_oper->xltype == xltypeStr) `
  
falharia nesse caso porque **xlbitDLLFree** está definido. 
  
Em geral, **xlAutoFree** e **xlAutoFree12** devem ser implementados para liberar memória associada a matrizes **xltypeMulti** criadas por XLL e referências **externas xltypeRef.** 
  
Você pode decidir implementar suas funções XLL para que todas elas retornem XLOPER e **XLOPER12s alocados dinamicamente.**  Nesse caso, você precisaria definir **xlbitDLLFree** em todos esses **XLOPER** e **XLOPER12** s, independentemente do subtipo. Você também precisaria implementar **xlAutoFree** e **xlAutoFree12** para que essa memória fosse liberada e também qualquer memória apontada dentro do **XLOPER** /  **XLOPER12**. Essa abordagem é uma maneira de tornar o thread de valor de retorno seguro. Por exemplo, a função anterior poderia ser reescrita da seguinte forma.
  
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

Para obter mais informações **sobre xlAutoFree** e **xlAutoFree12**, consulte [xlAutoFree/xlAutoFree12](xlautofree-xlautofree12.md).
  
## <a name="returning-modify-in-place-arguments"></a>Retornando argumentos modify-in-place

O Excel permite que uma função XLL retorne um valor modificando um argumento no local. Você só pode fazer isso com um argumento passado como um ponteiro. Para trabalhar assim, a função deve ser registrada de uma maneira que informa ao Excel qual argumento será modificado. 
  
Esse método de retornar um valor é suportado para todos os tipos de dados que podem ser passados por ponteiro, mas é especialmente útil para os seguintes tipos:
  
- Cadeias de caracteres de byte ASCII terminadas por tamanho e terminadas por caractere nulo
    
- Cadeias de caracteres largos Unicode contadas por tamanho e terminadas por caractere nulo (começando no Excel 2007)
    
- **Matrizes de** ponto flutuante FP 
    
- **Matrizes de ponto flutuante FP12** (a partir do Excel 2007) 
    
> [!NOTE]
> Você não deve tentar retornar **XLOPER** s ou **XLOPER12** s dessa maneira. Confira mais informações em [Problemas conhecidos no desenvolvimento de XLL do Excel](known-issues-in-excel-xll-development.md). 
  
A vantagem de usar essa técnica, em vez de apenas usar a instrução de retorno, é que o Excel aloca a memória para os valores de retorno. Depois que o Excel terminar de ler os dados retornados, ele liberará a memória. Isso retira as tarefas de gerenciamento de memória da função XLL. Essa técnica é thread-safe: se chamado simultaneamente pelo Excel em threads diferentes, cada chamada de função em cada thread tem seu próprio buffer.
  
É útil para os tipos de dados listados anteriormente, em particular, porque o mecanismo de chamada de volta para a DLL para liberar o pós-retorno de memória que existe para **XLOPER** XLOPER12 s não existe para cadeias de caracteres simples e matrizes /   **FP12** /  **FP12.** Portanto, ao retornar uma cadeia de caracteres criada por DLL ou uma matriz de ponto flutuante, você tem as seguintes opções: 
  
- De definir um ponteiro persistente para um buffer alocado dinamicamente, retorne o ponteiro. Na próxima chamada para a função (1), verifique se o ponteiro não é nulo, (2) libera os recursos alocados na chamada anterior e redefine o ponteiro como nulo, (3) reutiliza o ponteiro para um bloco de memória recém-alocado.
    
- Crie suas cadeias de caracteres e matrizes em um buffer estático que não precisa ser liberado e retorne um ponteiro para ele.
    
- Modifique um argumento no local, escrevendo sua cadeia de caracteres ou matriz diretamente no espaço reservado pelo Excel.
    
Caso contrário, você deve criar um /  **XLOPER XLOPER12** e usar **xlbitDLLFree** e **xlAutoFree** /  **xlAutoFree12** para liberar os recursos. 
  
A última opção pode ser a mais simples nesses casos em que você está sendo passado um argumento do mesmo tipo que o valor de retorno. O ponto-chave a ser lembrado é que os tamanhos de buffer são limitados e você deve ter muito cuidado para não ultrapassá-los. Fazer isso errado pode falhar no Excel. Os tamanhos de buffer para cadeias de **caracteres** e /  matrizes **FP12** serão discutidos em seguida. 
  
## <a name="strings"></a>Cadeias de caracteres

Os problemas com o gerenciamento de memória de cadeia de caracteres são, sem dúvida, a causa mais comum de instabilidade em aplicativos e complementos. Talvez seja compreensível, considerando as diversas maneiras pelas quais as cadeias de caracteres são tratadas: terminadas por caractere nulo ou contadas por tamanho (ou ambas); buffers estáticos ou dinâmicos; comprimento fixo ou comprimento quase ilimitado; memória gerenciada do sistema operacional (por exemplo, OLE Bstr) ou cadeias de caracteres não gerenciadas; e assim por diante.
  
Os programadores do C/C++ estão mais familiarizados com cadeias de caracteres terminadas por caracteres nulos. A biblioteca C padrão foi projetada para funcionar com essas cadeias de caracteres. Os literais de cadeia de caracteres estática no código são compilados em cadeias de caracteres terminadas por caractere nulo. Como alternativa, o Excel funciona com cadeias de caracteres contadas por tamanho que não estão em geral terminadas com nulo. A combinação desses fatos requer uma abordagem clara e consistente em sua DLL/XLL em relação a como você lida com cadeias de caracteres e memória de cadeia de caracteres.
  
Os problemas mais comuns são os seguinte:
  
- A passagem de um ponteiro nulo ou inválido para uma função que espera um ponteiro válido e não pode ou não verificar a validade do ponteiro em si.
    
- A sobresrução dos limites de um buffer de cadeia de caracteres por uma função que não verifica ou não o comprimento do buffer em relação ao comprimento da cadeia de caracteres que está sendo escrita.
    
- Tentar liberar memória de buffer de cadeia de caracteres que seja estática ou já tenha sido liberada ou não tenha sido alocada de maneira consistente com a forma como ela está sendo liberada.
    
- Vazamentos de memória resultantes da alocação de cadeias de caracteres e, em seguida, não liberados, geralmente em uma função frequentemente chamada.
    
### <a name="rules-for-strings"></a>Regras para cadeias de caracteres

Assim como **os** /  **XLOPER XLOPER** s, há regras e diretrizes que você deve seguir. As diretrizes são as mesmas fornecidas na seção anterior. As regras aqui são uma extensão das regras especificamente para cadeias de caracteres.
  
 **Regras:**
  
- Não tente liberar memória ou substituir a cadeia de /  caracteres **XLOPER XLOPER12** s ou cadeias de caracteres simples contadas por comprimento ou terminadas por nulo passadas como argumentos para sua função XLL. Você deve tratar esses argumentos como somente leitura.
    
- Onde o Excel aloca memória para uma cadeia de caracteres /  **XLOPER XLOPER12** para o valor de retorno de uma função de retorno de chamada da API C, use **xlFree** para libera-la ou defina **xlbitXLFree** se a retornar para o Excel a partir de uma função XLL. 
    
- Onde sua DLL aloca dinamicamente um buffer de cadeia de caracteres para um **XLOPER** XLOPER12 , livre-o de uma maneira consistente com a forma como você o alocou quando feito, ou de definir xlbitDLLFree se o retornar ao Excel a partir de uma função XLL e, em seguida, libera-lo em /   **xlAutoFree**  /  **xlAutoFree12**.
    
- Se o Excel tiver alocado memória para uma matriz **xltypeMulti** retornada para sua DLL em uma chamada para a API de C, não substituir qualquer cadeia de caracteres  /  **XLOPER XLOPER12** s dentro da matriz. Essas matrizes só devem ser liberadas usando **xlFree** ou, se retornadas por uma função XLL, definindo **xlbitXLFree**.
    
### <a name="string-types-supported"></a>Tipos de cadeia de caracteres com suporte

**C API xltypeStr XLOPER/XLOPER12s**

|Cadeias de caracteres de byte: **XLOPER****|**Cadeias de caracteres largos: **XLOPER12****|
|:-----|:-----|
|Todas as versões do Excel  <br/> |A partir do Excel 2007  <br/> |
|Comprimento máximo: 255 bytes ASCII estendidos  <br/> |Comprimento máximo de 32.767 caracteres Unicode  <br/> |
|Primeiro byte (não assinado) = comprimento  <br/> |Primeiro caractere Unicode = comprimento  <br/> |
   
> [!IMPORTANT]
> Não pressuporte a terminação nula **de cadeias** de caracteres **XLOPER ou XLOPER12.** 
  
**Cadeias de caracteres C/C++**

|**Cadeias de caracteres de byte**|**Cadeias de caracteres largos**|
|:-----|:-----|
|Terminada em nulo (**char** *) "C" Comprimento máximo: 255 bytes ASCII estendidos  <br/> |Terminada em nulo (**wchar_t** *) "C%" Comprimento máximo 32.767 caracteres Unicode  <br/> |
|Contada por tamanho (**caractere não assinado** *) "D"  <br/> |Contada por tamanho (**wchar_t** *) "D%"  <br/> |
   
### <a name="strings-in-xltypemulti-xloperxloper12-arrays"></a>Cadeias de caracteres em matrizes xltypeMulti XLOPER/XLOPER12

Em vários casos, o Excel cria uma **matriz xltypeMulti** para uso em sua DLL/XLL. Várias das funções de informações XLM retornam essas matrizes. Por exemplo, a função da API C **xlfGetWorkspace**, quando passada o argumento  *44*  , retorna uma matriz contendo cadeias de caracteres que descrevem todos os procedimentos de DLL registrados no momento. A função da API de C **xlfDialogBox** retorna uma cópia modificada de seu argumento de matriz, contendo cópias profundas das cadeias de caracteres. Talvez a maneira mais comum de um XLL encontrar uma matriz **xltypeMulti** é onde ela foi passada como um argumento para uma função XLL ou foi coerced para esse tipo a partir de uma referência de intervalo. Nesses últimos casos, o Excel cria cópias profundas das cadeias de caracteres nas células de origem e aponta para elas dentro da matriz. 
  
Onde você deseja modificar essas cadeias de caracteres em sua DLL, você deve fazer suas próprias cópias profundas. Ao criar suas próprias matrizes **xltypeMulti,** você não deve colocar a cadeia de caracteres **alocada** pelo Excel /  **XLOPER XLOPER12** s dentro delas. Isso correrá o risco de você não os liberar corretamente mais tarde ou não os liberar. Novamente, você deve fazer cópias profundas das cadeias de caracteres e armazenar ponteiros para as cópias na matriz.
  
 **Exemplos**
  
A função de exemplo a seguir cria uma cópia alocada dinamicamente de uma cadeia de caracteres Unicode contada por tamanho. Observe que o chamador deve, por fim, liberar a memória alocada neste exemplo usando **delete**[], e que a cadeia de caracteres de origem não é assumida como terminada como nula. A cadeia de caracteres de cópia é truncada, se necessário, para segurança e não é terminada em nulo.
  
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

Esta função pode ser usada com segurança para copiar um **XLOPER12**, conforme mostrado na seguinte função XLL exportável que retorna uma cópia de seu argumento se for uma cadeia de caracteres. Todos os outros tipos são retornados como uma cadeia de caracteres de comprimento zero. Observe que os intervalos não são manipulados — a função **retorna #VALUE!**. A função deve ser registrada como tendo um argumento de tipo U para que as referências sejam passadas como valores. Isso equivale à função de planilha **T(),** exceto pelo fato de que **AsText** também converte erros em cadeias de caracteres de comprimento zero. Este exemplo de código assume que **xlAutoFree12** libera o ponteiro passado e também seu conteúdo, usando **excluir**.
  
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

Argumentos registrados como tipos **F**, **G**, **F%** e **G%** podem ser modificados no local. Quando o Excel está preparando argumentos de cadeia de caracteres para esses tipos, ele cria um buffer de comprimento máximo. Em seguida, ele copia a cadeia de caracteres do argumento para isso, mesmo se essa cadeia de caracteres for muito mais curta. Isso permite que a função XLL escreva seu valor de retorno diretamente na mesma memória. 
  
Os tamanhos de buffer separados para esses tipos são os seguinte:
  
- **Cadeias de caracteres de bytes:** 256 bytes, incluindo o contador de comprimento (tipo G) ou terminação nula (tipo F). 
    
- **Cadeias de caracteres Unicode:** 32.768 caracteres de largura (65.536 bytes), incluindo o contador de comprimento (tipo G%) ou terminação nula (tipo F%). 
    
> [!NOTE]
> Você não pode chamar essa função diretamente do Visual Basic for Applications (VBA) porque não pode garantir que um buffer suficientemente grande tenha sido alocado. Você só pode chamar essa função de outra DLL com segurança se tiver passado explicitamente um buffer grande o suficiente. 
  
Aqui está um exemplo de uma função XLL que inverte uma cadeia de caracteres largos terminada em nulo usando a função de biblioteca **padrão wcsrev**. O argumento nesse caso seria registrado como tipo **F%**.
  
```cs
void WINAPI reverse_text_xl12(wchar_t *text)
{
    _wcsrev(text);
}
```

## <a name="persistent-storage-binary-names"></a>Armazenamento Persistente (Nomes Binários)

Os nomes binários são definidos e associados a blocos de binários, ou seja, não estruturados, dados armazenados junto com a agenda. Eles são criados usando a função [xlDefineBinaryName](xldefinebinaryname.md)e os dados são recuperados usando a função [xlGetBinaryName](xlgetbinaryname.md). Ambas as funções são descritas em mais detalhes na referência de função (consulte Funções da API C que podem ser chamadas apenas de uma DLL ou [XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)), e ambas usam **xltypeBigData** **XLOPER XLOPER12** /  . 
  
Para obter informações sobre problemas conhecidos que limitam as aplicações práticas de nomes binários, consulte Problemas conhecidos no [desenvolvimento de XLL do Excel.](known-issues-in-excel-xll-development.md)
  
## <a name="excel-stack"></a>Pilha do Excel

O Excel compartilha seu espaço em pilha com todas as DLLs carregadas. O espaço em pilha geralmente é mais do que adequado para uso comum, e você não precisa se preocupar com isso, contanto que siga algumas diretrizes: 
  
- Não passe estruturas muito grandes como argumentos para funções por valor na pilha. Passe ponteiros ou referências em vez disso.
    
- Não retorna estruturas grandes na pilha. Retorne ponteiros para memória estática ou alocada dinamicamente ou use argumentos passados por referência.
    
- Não declare estruturas variáveis automáticas muito grandes no código de função. Se você precisar deles, declare-os como estáticos.
    
- Não chame funções recursivamente, a menos que você tenha certeza de que a profundidade da recursão sempre será superficial. Tente usar um loop em vez disso.
    
Quando uma DLL liga de volta para o Excel usando a API de C, o Excel primeiro verifica se há espaço suficiente na pilha para a chamada de uso do pior caso que poderia ser feita. Se achar que pode haver espaço insuficiente, a chamada falhará por ser segura, mesmo que possa ter espaço suficiente para essa chamada específica. Nesse caso, os retornos de chamada retornam o código **xlretFailed**. Para uso comum da API de C e da pilha, essa é uma causa improvável da falha de uma chamada à API C.
  
Se você estiver preocupado, apenas curioso, ou quiser eliminar a falta de espaço em pilha como motivo de uma falha grave, poderá descobrir quanto espaço na pilha há com uma chamada para a função [xlStack.](xlstack.md) 
  
## <a name="see-also"></a>Confira também



[Recálculo com vários threads no Excel](multithreaded-recalculation-in-excel.md)
  
[Contenção de memória e multithreading no Excel](multithreading-and-memory-contention-in-excel.md)
  
[Desenvolvimento de XLLs do Excel](developing-excel-xlls.md)

