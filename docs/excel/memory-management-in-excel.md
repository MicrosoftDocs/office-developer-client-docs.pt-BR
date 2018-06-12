---
title: Gerenciamento de memória no Excel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
keywords:
- memória XLOPER12 [excel 2007], gerenciar memória no Excel, do Excel pilha, cadeias de caracteres [Excel 2007], gerenciamento de memória, gerenciamento de memória no Excel, memória XLOPER [Excel 2007], memória [Excel 2007], diretrizes de gerenciamento
localization_priority: Normal
ms.assetid: 3bf5195b-6235-43cf-8795-0c7b0a63a095
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 97c76d762fdc5e575c571804816e5581a7bec8bb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765429"
---
# <a name="memory-management-in-excel"></a>Gerenciamento de memória no Excel

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Gerenciamento de memória é a preocupação mais importante se você quiser criar XLLs eficientes e estáveis. Falha ao gerenciar memória também pode levar a um intervalo de problemas no Microsoft Excel — de pequenos problemas, como a alocação de memória ineficientes e inicialização e vazamento de memória pequeno, para os principais problemas, como o destabilization do Excel.
  
Mal gerenciamento de memória é a origem mais comuns de problemas sérios adicionar em relacionados. Portanto, você deve construir seu projeto com uma estratégia consistente e bem-planejado por meio de gerenciamento de memória. 
  
Gerenciamento de memória se tornou mais complexo no Microsoft Office Excel 2007 com a introdução de recálculo de pasta de trabalho multithread. Se você deseja criar e exportar as funções de planilha de thread-safe, você deve gerenciar os conflitos resultantes que podem ocorrer quando vários threads competem por acesso.
  
Há considerações de memória para os seguintes tipos de estrutura de dados de três:
  
- S **XLOPER**e **XLOPER12**s
    
- Cadeias de caracteres que não estão em um **XLOPER** ou **XLOPER12**
    
- Matrizes **FP** e **FP12** 
    
## <a name="xloperxloper12-memory"></a>Memória XLOPER/XLOPER12

**XLOPER**/ **XLOPER12** estrutura de dados tem algumas subtipos que contêm ponteiros para blocos de memória, notadamente cadeias de caracteres (**xltypeStr**), matrizes (**xltypeMulti**) e as referências externas (**xltypeRef**). Observe também que matrizes **xltypeMulti** podem conter a cadeia de caracteres **XLOPER**/ **XLOPER12s** que por sua vez apontam para outros blocos de memória. 
  
**XLOPER**/ **XLOPER12** podem ser criados de várias maneiras: 
  
- Pelo Excel ao preparar os argumentos a serem passados para uma função XLL
    
- Pelo Excel ao retornar um **XLOPER** ou **XLOPER12** em uma API C chamada 
    
- Por sua DLL ao criar argumentos a serem passados para uma API C chamada
    
- Por sua DLL ao criar uma função XLL do valor de retorno
    
Um bloco de memória em um dos tipos de memória apontando pode ser alocado de várias maneiras:
  
- Pode ser um bloco estático dentro da sua DLL fora qualquer código de função, caso em que você não precisará alocar ou liberar a memória.
    
- Pode ser um bloco estático dentro da sua DLL dentro de alguns códigos de função, caso em que você não precisará alocar ou liberar a memória.
    
- Ele pode ser dinamicamente alocado e liberado pela sua DLL de várias maneiras possíveis: **malloc** e **livres**, **novo** e **Excluir**e assim por diante.
    
- Ele pode ser alocado dinamicamente pelo Excel.
    
Dado o número de origens possíveis para **XLOPER**/ **XLOPER12** memória e o número de situações nas quais o **XLOPER**/ **XLOPER12** poderia gerar que atribuído a memória, não é surpreendente que esse assunto pode parece muito difícil. No entanto, a complexidade pode ser reduzida significativamente se você seguir várias regras e diretrizes. 
  
### <a name="rules-for-working-with-xloperxloper12"></a>Regras para trabalhar com XLOPER/XLOPER12

- Não tente liberar memória ou para substituí **XLOPERs**/ **XLOPER12**s são passados como argumentos para sua função XLL. Você deve tratar tais argumentos como somente leitura. Para obter mais informações, consulte "Retornando **XLOPER** ou **XLOPER12** pelos argumentos Modifying in-loco" em [Problemas conhecidos no desenvolvimento de XLL do Excel](known-issues-in-excel-xll-development.md).
    
- Se Excel tem memória alocada para **XLOPER**/ **XLOPER12** retornado para sua DLL em uma chamada para a API C: 
    
  - Você deve liberar a memória quando não precisar mais **XLOPER**/ **XLOPER12** usando uma chamada para [xlFree](xlfree.md). Não usar qualquer outro método, como gratuito ou excluir para liberar a memória.
    
  - Se o tipo retornado é **xltypeMulti**, não substituir qualquer **XLOPER**/ **XLOPER12**s dentro do conjunto, especialmente se eles contêm cadeias de caracteres, e especialmente não onde você está tentando substituir por uma cadeia de caracteres.
    
  - Se você deseja retornar **XLOPER**/ **XLOPER12** para o Excel como valor de retorno da função da DLL, você deve informar ao Excel que não há memória que o Excel deve liberar quando terminado. 
    
- Você só deve chamar **xlFree** em **XLOPER**/ **XLOPER12** que foi criado como o valor de retorno para uma chamada de API C. 
    
- Se sua DLL tem memória alocada para **XLOPER**/ **XLOPER12** que você deseja retornar ao Excel como valor de retorno da função da DLL, você deve informar ao Excel que não há memória a DLL deve liberar. 
    
### <a name="guidelines-for-memory-management"></a>Diretrizes para o gerenciamento de memória

- Seja consistente em seu DLL no método que você usa para alocar e liberar memória. Evite a combinação de métodos. Uma boa abordagem é quebrar o método que você está usando para cima em uma classe de memória ou a estrutura, dentro do qual você pode alterar o método usado sem alterar o seu código em muitos locais.
    
- Quando você criar matrizes **xltypeMulti** dentro da sua DLL, seja consistente da maneira que você alocar memória para as cadeias de caracteres: sempre dinamicamente alocar a memória para eles ou sempre use static memória. Se você fizer isso, quando você estiver liberando a memória, você saberá que você deve sempre ou nunca liberar as cadeias de caracteres. 
    
- Fazer cópias de profundidade de memória alocada para Excel quando você está copiando criados pelo Excel **XLOPER**/ **XLOPER12**.
    
- Não coloque alocadas Excel cadeia de caracteres **XLOPER**/ **XLOPER12**s dentro **xltypeMulti** matrizes. Faça cópias profundas das cadeias de caracteres e armazene ponteiros para as cópias na matriz. 
    
## <a name="freeing-excel-allocated-xloperxloper12-memory"></a>Liberar memória XLOPER/XLOPER12 alocada para Excel

Considere o seguinte comando XLL, que usa **xlGetName** para obter uma cadeia de caracteres contendo o nome de arquivo e o caminho da DLL e o exibe em uma caixa de diálogo alerta usando **xlcAlert**.
  
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

Quando a função não precisa mais a memória apontada pela **xDllName**, ele pode liberá-la usando uma chamada para a [função xlFree](xlfree.md), uma das funções somente DLL C API. 
  
A função **xlFree** é totalmente documentada na seção de referência de função (consulte [C API funções que pode ser chamado apenas por um DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)), mas esteja ciente das seguintes opções:
  
- Você pode passar ponteiros para mais de um **XLOPER**/ **XLOPER12**s em uma única chamada de **xlFree**, limitado somente pelo número de argumentos da função compatíveis com a versão em execução do Excel (30 no Excel 2003, 255 iniciada no Excel 2007).
    
- **xlFree** define o ponteiro contido como **Nulo** para garantir que uma tentativa de liberar um **XLOPER**/ **XLOPER12** que já foi liberada é seguro. **xlFree** é a única função de API C que modifica seus argumentos. 
    
- Você pode chamar com segurança **xlFree** em qualquer **XLOPER**/ **XLOPER12** usado para o valor de retorno de uma chamada para a API C, independentemente se ele contém um ponteiro para a memória. 
    
## <a name="returning-xloperxloper12s-to-be-freed-by-excel"></a>Retornando XLOPER/XLOPER12s serem liberados pelo Excel

Suponha que você queria modificar o comando de exemplo na seção anterior e alterá-la para uma função de planilha que retorna o caminho e nome da DLL quando passado um argumento **booleano** de **true** e **# N/d** caso contrário. Sem dúvida, você não pode chamar **xlFree** para liberar memória a cadeia de caracteres antes de retorná-la para o Excel. No entanto, se ela não é liberada em algum momento, o suplemento será vazamento de memória sempre que a função for chamada. Para contornar esse problema, você pode definir um pouco no campo **xltype** da **XLOPER**/ **XLOPER12**, definido como **xlbitXLFree** no xlcall. h. Essa configuração informa ao Excel que ele deve liberar a memória retornada quando ele tiver terminado, copiando o valor. 
  
### <a name="example"></a>Example

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

Funções XLL que usam **XLOPER**/ **XLOPER12**s deve ser declarada como levando e retornando ponteiros para **XLOPER**/ **XLOPER12**s. O uso neste exemplo de uma estática **XLOPER12** dentro da função não é thread-safe. Você pode registrar incorretamente dessa função como thread-safe, mas você poderia ser um risco **xRtnValue** sejam sobrescritos por um segmento antes de outro thread tinha concluído com ele. 
  
Você deve definir **xlbitXLFree** após a chamada para o retorno de chamada do Excel que aloca-lo. Se você defini-la antes que isso, ele será substituído e não tem o efeito que você deseja. Se você pretende usar o valor como um argumento em uma chamada para outra função do C API antes de retorná-la à planilha, você deve definir esse bit após qualquer tal chamada. Caso contrário, você irá confunda funções que não mascarar esse bit antes de verificar **XLOPER**/ **XLLOPER12** tipo. 
  
## <a name="returning-xloperxloper12s-to-be-freed-by-the-dll"></a>Retornando XLOPER/XLOPER12s serem liberados pela DLL

Um problema semelhante a isso ocorre quando o seu XLL tem memória alocada para **XLOPER**/ **XLOPER12** e quer retorná-lo para o Excel. O Excel reconhece outra bit que pode ser definida no campo **xltype** da **XLOPER**/ **XLOPER12**, definido como **xlbitDLLFree** em xlcall. h. 
  
Quando o Excel recebe **um XLOPER**/ **XLOPER12** com esse bit definido, ele tentará chamar uma função que deve ser exportada pelo XLL chamado [xlAutoFree](xlautofree-xlautofree12.md) (para **XLOPER**s) ou **xlAutoFree12** (para **XLOPER12**s). Essa função é descrita com mais detalhes na referência de função (consulte [Gerenciador de suplementos e funções da Interface XLL](add-in-manager-and-xll-interface-functions.md)), mas um exemplo de implementação mínimo é fornecido aqui. Seu objetivo é livre **XLOPER**/ **XLOPER12** memória de forma consistente com como ela foi originalmente alocada. 
  
### <a name="examples"></a>Exemplos

A função de exemplo a seguir faz o mesmo que a função anterior, exceto que inclui o texto "o nome do caminho completo para essa DLL é" antes do nome da DLL.
  
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

Uma implementação minimamente suficiente de **xlAutoFree12** em XLL que exportou a função anterior seria da seguinte maneira. 
  
```cs
void WINAPI xlAutoFree12(LPXLOPER12 p_oper)
{
    if(p_oper->xltype == (xltypeStr | xlbitDLLFree))
        free(p_oper->val.str);
}
```

Essa implementação é suficiente apenas se o XLL retorna apenas **XLOPER12** cadeias de caracteres, e essas cadeias de caracteres somente são alocadas usando **malloc**. Observe que o teste 
  
 ` if(p_oper->xltype == xltypeStr) `
  
falhará neste caso porque **xlbitDLLFree** está definido. 
  
Em geral, **xlAutoFree** e **xlAutoFree12** devem ser implementados para que eles liberar memória associada criados XLL **xltypeMulti** matrizes e **xltypeRef** as referências externas. 
  
Talvez você decida implementar suas funções XLL, para que eles todos retorno alocadas dinamicamente s **XLOPER**e **XLOPER12**s. Nesse caso, você precisaria definir **xlbitDLLFree** todos os tais s **XLOPER**e **XLOPER12**s independentemente do subtipo. Você também precisará implementar **xlAutoFree** e **xlAutoFree12** para que essa memória foi liberada e também qualquer memória apontado para dentro **XLOPER**/ **XLOPER12**. Essa abordagem é uma maneira de fazer o thread de valor de retorno seguros. Por exemplo, a função anterior poderia ser reescrita da seguinte maneira.
  
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

Para obter mais informações sobre **xlAutoFree** e **xlAutoFree12**, consulte [xlAutoFree/xlAutoFree12](xlautofree-xlautofree12.md).
  
## <a name="returning-modify-in-place-arguments"></a>Retornando argumentos modificar-in-loco

Excel permite que uma função XLL retornar um valor modificando um argumento in-loco. Você só pode fazer isso com um argumento passado como um ponteiro. Para trabalhar assim, a função deve ser registrada de forma que informa ao Excel qual argumento será modificado. 
  
Esse método de retornar um valor é suportado para todos os tipos de dados que podem ser passados pelo ponteiro, mas é especialmente útil para os seguintes tipos:
  
- Comprimento contado e terminada em nulo cadeias de caracteres de byte de ASCII
    
- Comprimento contado e terminada em nulo cadeias de caracteres longa de Unicode (começando no Excel 2007)
    
- Matrizes de ponto flutuante **FP** 
    
- Matrizes de ponto flutuante **FP12** (começando no Excel 2007) 
    
> [!NOTE]
> Você não deve tentar retornar **XLOPER**s ou s **XLOPER12**dessa maneira. Para obter mais informações, consulte [Problemas conhecidos no desenvolvimento de XLL do Excel](known-issues-in-excel-xll-development.md). 
  
A vantagem de usar essa técnica, em vez de usar apenas a instrução retornar, é que o Excel aloca a memória para os valores de retorno. Depois que o Excel concluiu a ler os dados retornados, ele libera a memória. Isso leva a memória para tarefas de gerenciamento, separando-a função XLL. Essa técnica é thread-safe: se chamado simultaneamente pelo Excel em threads diferentes, cada chamada de função em cada segmento tem seu próprio buffer.
  
É útil para os tipos de dados listados anteriormente em particular porque o mecanismo de chamada de volta a DLL para liberar memória POST-retornar que existe para **XLOPER**/ **XLOPER12**s não existe para cadeias de caracteres simples e **FP** /  Matrizes de **FP12** . Portanto, ao retornar uma cadeia de caracteres criada a DLL ou matriz de ponto flutuante, você tem as seguintes opções: 
  
- Definir um ponteiro persistente em um buffer alocado dinamicamente, o ponteiro de retorno. Na próxima chamada para a função (1) verificação de que o ponteiro não é nula (2) gratuito os recursos alocados na chamada anterior em Redefinir o ponteiro como null, (3) reutilização o ponteiro para um bloco recentemente alocado de memória.
    
- Crie seu cadeias de caracteres e matrizes em um buffer estático que não precisam ser liberados e retornar um ponteiro para que.
    
- Modifica um argumento in-loco, gravar sua cadeia de caracteres ou matriz diretamente para o espaço reservado pelo Excel.
    
Caso contrário, você deve criar um **XLOPER**/ **XLOPER12**e uso **xlbitDLLFree** e **xlAutoFree**/ **xlAutoFree12** para liberar os recursos. 
  
A última opção pode ser o mais simples nesses casos em que você está sendo um argumento do mesmo tipo passados como o valor de retorno. O ponto-chave lembrar é que os tamanhos de buffer são limitados e você deve tomar muito cuidado para não saturação-los. Obter isso errado poderia falha no Excel. Tamanhos de cadeias de caracteres e **FP**de buffer/ **FP12** matrizes são abordadas em Avançar. 
  
## <a name="strings"></a>Cadeias de caracteres

Problemas com o gerenciamento de memória de cadeia de caracteres relativamente são a causa mais comum de instabilidade em suplementos e aplicativos. É compreensível talvez, dado a várias maneiras em que as cadeias de caracteres são tratadas: terminada em nulo ou comprimento contado (ou ambos); buffers estáticos ou dinâmicos; comprimento fixo ou comprimento quase ilimitado; sistema operacional gerenciadas (por exemplo, denominadas Bstr OLE) de memória ou não gerenciadas cadeias de caracteres; e assim por diante.
  
Programadores C/C++ estão mais familiarizados com cadeias de caracteres terminada em nulo. A biblioteca C padrão é projetada para funcionar com essas cadeias de caracteres. Os literais de cadeia de caracteres estática no código são compilados em cadeias de caracteres terminada em nulo. Como alternativa, o Excel funciona com comprimento contado as cadeias de caracteres que não são em geral terminada em nulo. A combinação desses fatos requer uma abordagem clara e consistente dentro de sua DLL/XLL relacionadas a como você manipular cadeias de caracteres e memória de cadeia de caracteres.
  
Os problemas mais comuns são:
  
- A passagem de um ponteiro nulo ou inválido para uma função que espera um ponteiro válido e não aparecer ou não é possível verificar a validade do ponteiro em si.
    
- Saturar os limites de um buffer de cadeia de caracteres por uma função que não aparecer ou não é possível verificar o tamanho do buffer contra o comprimento da cadeia de caracteres que está sendo gravado.
    
- Tentando liberar memória de buffer de cadeia de caracteres que é estáticas, foi liberada já ou não foi alocada de forma que é consistente com como está sendo liberada.
    
- O vazamento de memória que resultam de cadeias de caracteres que está sendo alocado e, em seguida, não liberada, geralmente em uma função chamada com frequência.
    
### <a name="rules-for-strings"></a>Regras de cadeias de caracteres

Como ocorre com **XLOPER**/ s**XLOPER**, há regras e diretrizes que você deve seguir. As diretrizes são os mesmos determinado na seção anterior. As regras aqui são uma extensão das regras especificamente para as cadeias de caracteres.
  
 **Regras:**
  
- Não tente liberar memória ou substituir a cadeia de caracteres **XLOPER**/ **XLOPER12**s ou simples cadeias de caracteres de comprimento contado ou terminada em nulo passados como argumentos para sua função XLL. Você deve tratar tais argumentos como somente leitura.
    
- Onde o Excel aloca memória para uma cadeia de caracteres **XLOPER**/ **XLOPER12** para o valor de retorno de uma função de retorno de chamada da API C, use **xlFree** para liberá-la ou definir **xlbitXLFree** se retorná-lo para o Excel de uma função XLL. 
    
- Onde sua DLL dinamicamente aloca um buffer de cadeia de caracteres para um **XLOPER**/ **XLOPER12**, liberá-la de forma consistente com como alocado-lo quando feito ou defina **xlbitDLLFree** se retorná-lo para o Excel de uma função XLL e, em seguida, liberá-la em **xlAutoFree** /  **xlAutoFree12**.
    
- Se o Excel tem memória alocada para uma matriz de **xltypeMulti** retornada para sua DLL em uma chamada para a API C, não substituir qualquer cadeia de caracteres **XLOPER**/ **XLOPER12**s dentro da matriz. Tais matrizes somente devem ser liberados usando **xlFree**, ou, se estiver sendo retornados por uma função XLL, definindo **xlbitXLFree**.
    
### <a name="string-types-supported"></a>Tipos de cadeia de caracteres com suporte

**C API xltypeStr XLOPER/XLOPER12s**

|* * Cadeias de caracteres byte: * * XLOPER * * *|* * Larga cadeias de caracteres: * * XLOPER12 * * *|
|:-----|:-----|
|Todas as versões do Excel  <br/> |Iniciando no Excel 2007  <br/> |
|Comprimento máximo: 255 estendido bytes ASCII  <br/> |Comprimento máximo 32.767 caracteres Unicode  <br/> |
|Primeiro byte (não assinado) = comprimento  <br/> |Primeiro caractere Unicode = comprimento  <br/> |
   
> [!IMPORTANT]
> Não presuma finalização null das cadeias de caracteres **XLOPER** ou **XLOPER12** . 
  
**Cadeias de caracteres do C/C++**

|**Cadeias de caracteres de byte**|**Cadeias de caracteres longa**|
|:-----|:-----|
|Terminada em nulo (**char** *) "C" comprimento máximo: 255 estendido bytes ASCII  <br/> |Terminada em nulo (**wchar_t** *) "C %" comprimento de máximo 32.767 caracteres Unicode  <br/> |
|Comprimento contado (**não assinados char** *) "D"  <br/> |Comprimento contado (**wchar_t** *) "D %"  <br/> |
   
### <a name="strings-in-xltypemulti-xloperxloper12-arrays"></a>Cadeias de caracteres em xltypeMulti XLOPER/XLOPER12 matrizes

Em alguns casos, o Excel criará uma matriz **xltypeMulti** para uso na sua DLL/XLL. Várias das funções de informações de XLM retornam tais matrizes. Por exemplo, a API C função **xlfGetWorkspace**, quando passados o argumento *44* , retorna uma matriz que contém as cadeias de caracteres que descrevem todos os procedimentos DLL registrados no momento. A função do C API **xlfDialogBox** retorna uma cópia de modificação do seu argumento de matriz, contendo as cópias profundas das cadeias de caracteres. Talvez a maneira mais comum de que um XLL encontra uma matriz **xltypeMulti** é onde ele foi passado como um argumento para uma função XLL ou foi forçado a esse tipo de uma referência de intervalo. Nesses casos último, o Excel cria cópias profundas das cadeias de caracteres nas células de origem e pontos a essas dentro da matriz. 
  
Onde você deseja modificar essas cadeias de caracteres na sua DLL, você deve fazer seus próprios cópias profundas. Quando você estiver criando seus próprio matrizes **xltypeMulti** , você não deve colocar a cadeia de caracteres alocado pelo Excel **XLOPER**/ **XLOPER12**s dentro deles. Os riscos não liberando corretamente mais tarde, ou não dispensando-los. Novamente, você deve fazer cópias profundas das cadeias de caracteres e armazenar ponteiros para as cópias na matriz.
  
 **Exemplos**
  
A função de exemplo a seguir cria uma cópia alocada dinamicamente de uma cadeia de caracteres Unicode de comprimento contado. Observe que o chamador basicamente deve liberar a memória alocada neste exemplo usando [] de **Excluir**, e que a cadeia de caracteres de origem não é assumida como nulo encerrada. A cadeia de caracteres de cópia será truncada se necessário para segurança e não for nula finalizada.
  
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

Essa função, em seguida, pode ser usada com segurança para copiar **XLOPER12**, conforme mostrado na seguinte exportável XLL função que retorna uma cópia do seu argumento se ele for uma cadeia de caracteres. Todos os outros tipos são retornados como uma cadeia de caracteres de comprimento zero. Observe que os intervalos não são manipulados — a função retornará **#VALUE!**. A função deve ser registrada como colocar um argumento de tipo U para que as referências são passadas como valores. Isso é equivalente à função de planilha internas **T()** , exceto que **AsText** também converte erros em cadeias de caracteres de comprimento zero. Este exemplo de código pressupõe que **xlAutoFree12** libera o ponteiro no passado e também seu conteúdo, usando a **Excluir**.
  
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

### <a name="returning-modify-in-place-string-arguments"></a>Retornando argumentos de cadeia de caracteres de modificar-in-loco

Argumentos são registrados como tipos **F**, **G**, **F %** e **% G** podem ser modificados no lugar. Quando o Excel está preparando argumentos de cadeia de caracteres para esses tipos, ele cria um buffer de tamanho máximo. Em seguida, ele copia a cadeia de caracteres de argumento para que, mesmo se esta cadeia de caracteres é muito menor. Isso permite que a função XLL gravar seu valor de retorno diretamente para a mesma memória. 
  
Tamanhos de buffer isolam para esses tipos são:
  
- **Cadeias de caracteres de byte:** 256 bytes incluindo o contador de comprimento (tipo G) ou finalização null (tipo F). 
    
- **Cadeias de caracteres Unicode:** 32.768 ampla caracteres (65.536 bytes) incluindo o contador de comprimento (% de tipo G) ou finalização null (tipo F %). 
    
> [!NOTE]
> Você não pode chamar tal função diretamente do Visual Basic for Applications (VBA) porque você não pode garantir que um buffer suficientemente grande foi alocado. Você só pode chamar tal função a partir de outro DLL com segurança se você tiver passado explicitamente um buffer grande o suficiente. 
  
Aqui está um exemplo de uma função XLL que reverte uma cadeia de caracteres passada em caracteres terminada em nulo ampla usando a função de biblioteca padrão **wcsrev**. O argumento neste caso seria ser registrado como tipo **F %**.
  
```cs
void WINAPI reverse_text_xl12(wchar_t *text)
{
    _wcsrev(text);
}
```

## <a name="persistent-storage-binary-names"></a>Armazenamento persistente (nomes de binários)

Nomes de binários são definidos e associados blocos de binário, ou seja, os dados não estruturados, que são armazenados em conjunto com a pasta de trabalho. Eles são criados usando a função [xlDefineBinaryName](xldefinebinaryname.md)e os dados são recuperados usando a função [xlGetBinaryName](xlgetbinaryname.md). Ambas as funções são descritas em mais detalhes na referência de função (consulte [C API funções que pode ser chamado apenas por um DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)), e ambos usam **xltypeBigData** **XLOPER**/ **XLOPER12**. 
  
Para obter informações sobre problemas conhecidos que limitam as aplicações práticas de nomes de binários, consulte [Problemas conhecidos no desenvolvimento de XLL do Excel](known-issues-in-excel-xll-development.md).
  
## <a name="excel-stack"></a>Pilha do Excel

Excel compartilha seu espaço de pilha com todas as DLLs que ele tenha carregado. Espaço em pilha geralmente é mais do que adequado para uso comum, e você não precisará se preocupar com ele, desde que você seguir algumas diretrizes: 
  
- Não passe estruturas muito grandes como argumentos às funções pelo valor na pilha. Passe ponteiros ou referências em vez disso.
    
- Não retornam estruturas grandes na pilha. Retornam ponteiros para memória estática ou alocada dinamicamente ou usar os argumentos passados por referência.
    
- Não declare muito grandes estruturas variáveis automáticas no código de função. Se você precisar deles, declare-las como estático.
    
- Não chame funções recursivamente menos que tenha certeza de que a profundidade de recursão sempre será superficial. Tente usar um loop em vez disso.
    
Quando uma DLL chama de volta para o Excel usando a API C, o Excel primeiro verifica se há espaço suficiente na pilha para a chamada de pior caso de uso que poderia ser feita. Se ele achar que pode haver espaço insuficiente, ele falhará a chamada para ser seguro, mesmo que realmente tenha sido espaço suficiente para essa chamada específica. Nesse caso, os retornos de chamada retornam o código **xlretFailed**. Para uso comum da API C e a pilha de itens, esse é um improvável motivo da falha de uma chamada de API C.
  
Se você estiver preocupado ou apenas curioso, ou você deseja eliminar falta de espaço em pilha como um motivo para uma falha inexplicado, você pode descobrir quanto espaço de pilha lá está com uma chamada para a função [xlStack](xlstack.md) . 
  
## <a name="see-also"></a>Confira também



[Recálculo multithreaded no Excel](multithreaded-recalculation-in-excel.md)
  
[Multithreading e contenção de memória no Excel](multithreading-and-memory-contention-in-excel.md)
  
[Developing Excel XLLs](developing-excel-xlls.md)

