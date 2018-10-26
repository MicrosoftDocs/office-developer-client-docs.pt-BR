---
title: xlfRegister (Formato 1)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfRegister
keywords:
- função xlfregister [excel 2007]
localization_priority: Normal
ms.assetid: c730124c-1886-4a0f-8f06-79763025537d
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 3cd2e5072c8602fe301028e69592220a8345c211
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385078"
---
# <a name="xlfregister-form-1"></a>xlfRegister (Formato 1)

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Pode ser chamado de um comando DLL ou XLL que, por sua vez, foi chamado pelo Microsoft Excel. Equivale a chamar **REGISTER** de uma planilha de macro XLM do Excel. 
  
**xlfRegister** pode ser chamado em dois formatos: 
  
- xlfRegister (Formato 1): registra uma função ou comando único.
    
- [xlfRegister (Formato 2)](xlfregister-form-2.md): carrega e ativa um XLL.
    
Quando esta função é chamada no Formato 1, ela disponibiliza um comando ou função DLL para o Excel, define a contagem de uso como 1 e retorna a ID de registro, que pode ser usada para chamar a função posteriormente usando a função [xlUDF](xludf.md) ou **xlfCall**. A ID de registro também é usada para cancelar o registro da função usando [xlfUnregister (Formato 1)](xlfunregister-form-1.md). Se a função tiver sido registrada, chamar **xlfRegister** novamente incrementará a contagem de uso. 
  
Esse formato da função também define um nome oculto, que é o argumento de texto de função, _pxFunctionText_, e que é avaliado como ID de registro do comando ou da função. Quando cancelar o registro da função, exclua esse nome usando [xlfSetName](xlfsetname.md). Confira mais informações em [Problemas conhecidos no desenvolvimento de XLL do Excel](known-issues-in-excel-xll-development.md).
  
```cs
Excel12(xlfRegister, LPXLOPER12 pxRes, int iCount,
    LPXLOPER12 pxModuleText,   LPXLOPER12 pxProcedure,
    LPXLOPER12 pxTypeText,     LPXLOPER12 pxFunctionText,
    LPXLOPER12 pxArgumentText, LPXLOPER12 pxMacroType,
    LPXLOPER12 pxCategory,     LPXLOPER12 pxShortcutText,
    LPXLOPER12 pxHelpTopic,    LPXLOPER12 pxFunctionHelp,
    LPXLOPER12 pxArgumentHelp1, LPXLOPER12 pxArgumentHelp2,
        ...);
```

## <a name="parameters"></a>Parâmetros

_pxModuleText_ (**xltypeStr**)
  
O nome da DLL que contém a função. Pode ser obtido chamando a função somente XLL [xlGetName](xlgetname.md) se a função registrada também for membro da DLL atualmente em execução. 
  
_pxProcedure_ (**xltypeStr** ou **xltypeNum**)
  
Se cadeia de caracteres, o nome da função a chamar conforme aparece no código DLL. Se número, o número de exportação ordinal da função a chamar. Por motivos de clareza, use sempre o formato de cadeia de caracteres.
  
_pxTypeText_ (**xltypeStr**)
  
Uma cadeia de caracteres opcional que especifica os tipos de argumentos para a função e o tipo do valor de retorno da função. Confira mais informações na seção Comentários. Esse argumento pode ser omitido para uma DLL independente (XLL) que inclua uma [função xlAutoRegister](xlautoregister-xlautoregister12.md) ou **xlAutoRegister12**. 
  
> [!NOTE]
> **xlAutoRegister12** só tem suporte no Excel 2007. 
  
Se este argumento estiver ausente na chamada de **xlfRegister**, o Excel chamará **xlAutoRegister** ou **xlAutoRegister12**, caso qualquer dos dois exista na DLL especificada, o que deverá então registrar corretamente a função com o fornecimento dessas informações.
  
_pxFunctionText_ (**xltypeStr**)
  
O nome da função conforme aparecerá no Assistente de Função. Esse argumento é opcional. Se for omitido, a função ficará indisponível no Assistente de Função e só poderá ser chamada por meio da função **CALL** usando a ID de registro de funções de uma planilha de macro XLM. Portanto, para o uso comum de planilhas, você deve tratar esse argumento conforme exigido. 
  
_pxArgumentText_ (**xltypeStr**)
  
Uma cadeia de texto opcional que descreve os argumentos para a função. Aparece para o usuário no Assistente de Função. Se for omitida, o Excel construirá descrições básicas usando _pxTypeText_.
  
_pxMacroType_ (**xltypeNum** ou **xltypeInt**)
  
Um argumento opcional que indica o tipo do ponto de entrada XLL. Em caso de omissão, o valor padrão será 1.
  
|||||
|:-----|:-----|:-----|:-----|
| _Valor de pxMacroType_ <br/> |0  <br/> |1  <br/> |2  <br/> |
|Pode ser chamada de uma planilha  <br/> |Sim  <br/> |Sim  <br/> |Não  <br/> |
|Pode ser chamada de uma planilha de macro  <br/> |Sim  <br/> |Sim  <br/> |Sim  <br/> |
|Pode ser chamada de uma definição de nome definido  <br/> |Sim  <br/> |Sim  <br/> |Sim  <br/> |
|Pode ser chamada de uma expressão de formato condicional  <br/> |Sim  <br/> |Sim  <br/> |Não  <br/> |
|Listada no Assistente de Função para as funções de planilha  <br/> |Não  <br/> |Sim  <br/> |Não  <br/> |
|Listada no Assistente de Função para as funções de planilha de macro  <br/> |Não  <br/> |Sim  <br/> |Sim  <br/> |
   
Na prática, você deverá usar 1 para as funções de planilha, 1 para as funções equivalentes a planilhas de macro (registradas como tipo **#**) que você deseja chamar da planilha, e 2 para os comandos. 
  
> [!NOTE]
> Os comandos XLL ficam ocultos e não são exibidos nas caixas de diálogo para macros em execução, embora seus nomes possam ser inseridos em qualquer lugar em que um nome de comando válido seja necessário. 
  
_pxCategory_ (**xltypeStr** ou **xltypeNum**)
  
Um argumento opcional que permite especificar a qual categoria o novo comando ou função deve pertencer. O Assistente de Função divide as funções por tipo (categoria). É possível especificar um nome de categoria ou um número sequencial, em que o número representa a posição em que a categoria é exibida no Assistente de Função. Confira mais informações na seção “Nomes de Categoria”. Em caso de omissão, será usada a categoria Definido pelo Usuário.
  
_pxShortcutText_ (**xltypeStr**)
  
Uma cadeia de caracteres de caractere único, que diferencia maiúsculas de minúsculas, e que especifica a tecla de controle atribuída a esse comando. Por exemplo, “A” atribui esse comando a Control+Shift+A. Esse argumento é opcional e usado apenas para comandos.
  
_pxHelpTopic_ (**xltypeStr**)
  
Uma referência opcional para exibição no arquivo de Ajuda (.chm ou .hlp) quando o usuário clicar no botão de Ajuda (quando sua função personalizada é exibida). Pode ser no formato `filepath!HelpContextID` ou `https://address/path_to_file_in_site!0`. As duas partes antes e depois de “!” são necessárias.  *HelpContextID* não deve conter aspas simples e será convertida pelo Excel em um inteiro não assinado de 4 bytes de comprimento, no formato decimal. Ao usar o formato de URL, o Excel abrirá somente o arquivo de ajuda referenciado. 
  
_pxFunctionHelp_ (**xltypeStr**)
  
Uma cadeia de caracteres opcional que, ao ser selecionada no Assistente de Função, descreve a função que você personalizou.
  
_pxArgumentHelp1_ (**xltypeStr**)
  
Opcional. A primeira das cadeias de caracteres que descreve os argumentos personalizados da função quando esta é selecionada no Assistente de Função. No Excel 2003 e versões anteriores, **xlfRegister** pode aceitar, no máximo, 30 argumentos para que você possa fornecer essa ajuda apenas para os 20 primeiros de seus argumentos da função. Desde o Excel 2007, **xlfRegister** pode aceitar até 255 argumentos para que você possa fornecer essa ajuda para até 245 parâmetros de função. 
  
## <a name="property-valuereturn-value"></a>Valor de propriedade/Valor de retorno

Se o registro tiver sido bem-sucedido, essa função retornará a ID de registro da função (**xltypeNum**), que pode ser usada em chamadas para **xlUDF** e **xlfUnregister** na DLL, ou com **CALL** e **UNREGISTER** em uma planilha de macro XLM. Caso contrário, retornará um erro #VALUE! 
  
## <a name="remarks"></a>Comentários

### <a name="data-types"></a>Tipos de dados

O argumento _pxTypeText_ especifica o tipo de dados do valor de retorno e os tipos de dados de todos os argumentos para o recurso de código ou função DLL. O primeiro caractere de _pxTypeText_ especifica o tipo de dados do valor de retorno. Os caracteres restantes indicam os tipos de dados de todos os argumentos. Por exemplo, uma função DLL que retorne um número de ponto flutuante e aceite como argumento um número de ponto flutuante e um inteiro exigiria “BIB” para o argumento _pxTypeText_. 
  
As estruturas e os tipos de dados usados pelo Excel para trocar dados com XLLs estão resumidos nas duas tabelas a seguir.
  
A primeira tabela lista os tipos que têm suporte em todas as versões do Excel.
  
|**Tipo de dados**|**Passar por valor**|**Passar por ref (ponteiro)**|**Comentários**|
|:-----|:-----|:-----|:-----|
|Boolean  <br/> |A  <br/> |L  <br/> |curto [int] (0 = falso ou 1 = verdadeiro)  <br/> |
|double  <br/> |B  <br/> |E  <br/> ||
|char \*  <br/> ||C, F  <br/> |Cadeia de caracteres de bytes ASCII terminada por caractere nulo  <br/> |
|unsigned char \*  <br/> ||D, G  <br/> |Cadeia de caracteres de bytes ASCII contada  <br/> |
|unsigned short [int]  <br/> |H  <br/> ||WORD de 16 bits  <br/> |
|[signed] short [int]  <br/> |I  <br/> |M  <br/> |Inteiro assinado de 16 bits  <br/> |
|[signed long] int  <br/> |J  <br/> |N  <br/> |Inteiro assinado de 32 bits  <br/> |
|FP  <br/> ||K  <br/> |Estrutura de matriz do ponto flutuante  <br/> |
|Array  <br/> ||O  <br/> |São passados três argumentos:<br/>– unsigned short int \*<br/>– unsigned short int \*<br/>– double []  <br/> |
|XLOPER  <br/> ||P  <br/> |Valores e matrizes de planilha de tipo variável  <br/> |
|||R  <br/> |Referências de valores, matrizes e intervalos  <br/> |
   
No Excel 2007, os seguintes tipos de dados foram introduzidos para dar suporte às grades maiores e às cadeias de caracteres Unicode extensas.
  
|**Tipo de dados**|**Passar por valor**|**Passar por ref (ponteiro)**|**Comentários**|
|:-----|:-----|:-----|:-----|
|unsigned short \*  <br/> ||C%, F%  <br/> |Cadeia de caracteres largos Unicode terminada por caractere nulo  <br/> |
|unsigned short \*  <br/> ||D%, G%  <br/> |Cadeia de caracteres largos Unicode contada  <br/> |
|FP12  <br/> ||K%  <br/> |Estrutura de matriz do ponto flutuante de grade maior  <br/> |
|Array  <br/> ||O%  <br/> |São passados três argumentos:<br/>– signed int \* / RW \*<br/>– signed int \* / COL \*<br/>– double []  <br/> |
|XLOPER12  <br/> ||Q  <br/> |Valores e matrizes de planilha de tipo variável  <br/> |
|||U  <br/> |Referências de valores, matrizes e intervalos  <br/> |
   
Desde o Excel 2010, foram introduzidos os seguintes tipos de dados:
  
|**Tipo de dados**|**Passar por valor**|**Passar por ref (ponteiro)**|**Comentários**|
|:-----|:-----|:-----|:-----|
|XLOPER12  <br/> ||X  <br/> |O identificador assíncrono é usado para acompanhar uma chamada pendente de função assíncrona pelo Excel e XLL. A existência do tipo de parâmetro na cadeia de caracteres de tipo também designa a função como assíncrona. Confira mais informações sobre as funções assíncronas em [Funções assíncronas definidas pelo usuário](asynchronous-user-defined-functions.md).  <br/> |
   
Os tipos de cadeia de caracteres **F**, **F%**, **G** e **G%** são usados para os argumentos que são modificados no local. 
  
Ao trabalhar com os tipos de dados exibidos na tabela anterior, tenha em mente o seguinte:
  
- As declarações da linguagem C partem do princípio de que o compilador usa, por padrão, duplos de 8 bytes, inteiros curtos de 2 bytes e inteiros longos de 4 bytes.
    
- Todas as funções em DLLs e em recursos de códigos são chamadas por meio da convenção de chamada **__stdcall**. 
    
- Toda função que retorne um tipo de dados por referência, ou seja, que retorne um ponteiro para algo, pode retornar com segurança um ponteiro nulo. O Excel interpretará um ponteiro nulo como um erro #NUM!
    
## <a name="additional-data-type-information"></a>Informações adicionais sobre tipos de dados

Esta seção contém informações detalhadas sobre os tipos de dados **E**, **F**, **F%**, **G**, **G%**, **K**, **O**, **P**, **Q**, **R** e **U** e outras informações sobre o argumento _pxTypeText_. 
  
### <a name="e-data-type"></a>Tipo de dados E

O Excel espera que uma DLL que usa o tipo de dados E passe ponteiros para números de ponto flutuante na pilha. Isso pode causar problemas com certas linguagens (por exemplo, Borland C++) que esperam que o número seja passado na pilha emuladora do co-processador. A solução alternativa é passar um ponteiro para o número na pilha do coprocessador. O exemplo a seguir mostra como retornar um duplo do Borland C++.
  
```cpp
typedef double * lpDbl;
extern "C" lpDbl __stdcall AddDbl(double D1,
    double D2, WORD npDbl)
{
    lpDbl Result;
    Result = (lpDbl)MK_FP(_SS, npDbl);
    *Result = D1 + D2;
    return (Result);
}
```

### <a name="f-f-g-and-g-data-types"></a>Tipos de dados F, F%, G e G%

Com os tipos de dados **F**, **F%**, **G** e **G %**, uma função pode modificar um buffer de cadeia de caracteres alocado pelo Excel. Se o código do tipo de valor de retorno for um desses tipos, o Excel ignorará o valor retornado pela função. Em lugar disso, ele pesquisará na lista de argumentos de função o primeiro tipo de dados correspondente (**F**, **F%**, **G** ou **G%**) e usará os conteúdos atuais do buffer alocado da cadeia de caracteres como valor de retorno. Todas as versões do Excel alocam 256 bytes para as cadeias de caracteres ASCII **F** e **G** e, desde o Excel 2007, 65.536 bytes são alocados, o suficiente para 32.768 caracteres Unicode, para cadeias de caracteres Unicode **F%** e **G%**. Lembre-se de que os buffers devem incluir um caractere de contagem (tipos **G** e **G%**) ou um caractere de terminação nula (tipos **F** e **F%**) para que as extensões máximas reais da cadeia de caracteres sejam de 255 e 32.767. As cadeias de caracteres Unicode e, portanto, os argumentos do tipo **F%** e **G%** estão disponíveis apenas através da API C no Excel. 
  
### <a name="k-and-k-data-types"></a>Tipos de dados K e K%

Os tipos de dados **K** e **K%** usam ponteiros para as estruturas FP e FP12 de tamanhos variáveis, respectivamente. Esses estruturas são definidas em XLLCALL.H. As estruturas FP12 e, portanto, os argumentos do tipo **K%**, têm suporte apenas no Excel 2007 e versões posteriores. 
  
### <a name="o-and-o-data-types"></a>Tipos de dados O e O%

Os tipos de dados **O** e **O%** só podem ser usados para argumentos, e não para valores de retorno, embora os valores possam ser retornados com a modificação de um argumento do tipo **O** ou **O%** no local. Cada um passa três itens: um ponteiro para o número de linhas em uma matriz, um ponteiro para o número de colunas em uma matriz e um ponteiro para uma matriz bidimensional de números de ponto flutuante. 
  
Para modificar uma matriz passada pelo tipo de dados O ou O% no local, você poderia usar “>O” ou “>O%” como argumento _pxTypeText_. Confira mais informações sobre como modificar uma matriz na seção “Modificação no local: funções declaradas como nulas” deste tópico. 
  
O tipo de dados **O** foi criado para ter compatibilidade direta com DLLs do Fortran, que passam argumentos por referência. 
  
O **O%** tem suporte a partir do Excel 2007 e acomoda o maior número de linhas a que o Excel pode dar suporte. 
  
### <a name="p-and-q-data-types"></a>Tipos de dados P e Q

Quando o registro dos argumentos da função DLL usa o tipo XLOPERs**P** ou o tipo XLOPER12s **Q**, o Excel converte as referências de célula única para valores simples e as referências de várias células para matrizes na preparação destes argumentos. Ou seja, os tipos **P** e **Q** sempre chegarão à sua função como um destes tipos: **xltypeNum**, **xltypeStr**, **xltypeBool**, **xltypeErr**, **xltypeMulti**, **xltypeMissing** ou **xltypeNil**, exceto **xltypeRef** ou **xltypeSRef**, visto que estes são sempre desreferenciados. **XLOPER12**s e, portanto, os argumentos do tipo **Q**, têm suporte apenas no Excel 2007 e versões posteriores. 
  
Se os tipos **xltypeMissing** ou **xltypeNil** forem usados para valores de retorno, serão interpretados pelo Excel como zero numérico. **xltypeMissing** é passado quando o chamador omite um argumento. **xltypeNil** é passado quando o chamador passa uma referência a uma célula vazia. Quando um intervalo de células é convertido para **xltypeMulti** para ser passado como tipo **P** ou **Q**, toda célula em branco dentro do intervalo será convertida para elementos de matriz **xltypeNil**. Os elementos ausentes em uma matriz literal serão passados da mesma forma que elementos **xltypeNil**. 
  
### <a name="volatile-functions-and-recalculation"></a>Funções voláteis e recálculo

Em uma planilha, é possível tornar volátil um recurso de código ou função DLL para que haja um recálculo sempre que a planilha for recalculada. Para fazer isso, adicione um ponto de exclamação (!) após o último código de argumento no argumento _pxTypeText_. 
  
> [!NOTE]
> Por padrão, as funções que usam o tipo XLOPERs **R** ou o tipo XLOPER12s **U** e que são registradas como equivalentes a planilhas de macro (tipo **#**; conferir próxima seção) são tratadas como voláteis no Excel. 
  
### <a name="functions-declared-as-void"></a>Funções declaradas como nulas

Há duas situações que exigem a declaração de uma função como retorno nulo. Em ambos os casos, a função retorna o resultado por outros meios.
  
#### <a name="modifying-in-place"></a>Modificação no local

Você pode usar um único dígito _n_ para o código do tipo de retorno em _pxTypeText_, em que _n_ é um número entre 1 e 9. Isso instrui o Excel a usar como valor de retorno o valor da variável no local indicado pelo argumento _n_th em _pxTypeText_. Isso também é conhecido como modificação no local. O argumento _n_th deve ser um tipo de dados que passa por referência (C, D, E, F, F%, G, G%, K, K%, L, M, N, O, O%, P, Q, R ou U). O recurso de código ou função DLL também deve ser declarado com a palavra-chave **nulo** nas linguagens C++ (ou a palavra-chave **procedimento** na linguagem Pascal). 
  
Por exemplo, uma função DLL que usa como argumentos uma cadeia terminada por caractere nulo e dois ponteiros para inteiros pode modificar a cadeia no local. Use “1FMM” como argumento _pxTypeText_ e declare a função como nula. 
  
Versões anteriores do Excel usavam**\>** no início de _pxTypeText_ para indicar que a função tinha sido declarada como nula e que o primeiro argumento devia ser modificado no local; só era possível modificar o primeiro argumento. O **\>** equivale a _n_ = 1 em versões atuais do Excel e este uso de **\>** em funções síncronas tem suporte apenas para compatibilidade com versões anteriores. 
  
#### <a name="asynchronous-functions"></a>Funções assíncronas

Uma função assíncrona, indicada pelo uso de um parâmetro do tipo X em **pxTypeText**, não retornará o resultado da chamada de função inicial. Em vez disso, é necessário declarar uma função assíncrona como nula e posteriormente o suplemento retornará o resultado por meio de um retorno de chamada. A função assíncrona deve ser registrada usando **\>** no início de **pxTypeText**. Em funções assíncronas, **\>** indica que a função é declarada como nula, mas não indica que o primeiro argumento seja modificado no local. Confira mais informações sobre funções assíncronas em [Funções assíncronas definidas pelo usuário](asynchronous-user-defined-functions.md). 

### <a name="registering-worksheet-functions-as-macro-sheet-equivalents-handling-uncalculated-cells"></a>Registro de funções de planilha como equivalentes de planilha de macro (tratar células não calculadas)

Colocar um caractere **#** após o último código de parâmetro em _pxTypeText_ concede à função as mesmas permissões de chamada que as funções em uma planilha de macro. Da seguinte maneira: 
  
- A função pode recuperar os valores ainda não calculados das células no ciclo de recálculo.
    
- A função pode chamar qualquer função das informações XLM (classe 2), por exemplo, **xlfGetCell**.
    
- Se o sinal de número (#) não estiver presente: avaliar uma célula não calculada resultará em um erro **xlretUncalced** e a função atual será chamada novamente depois que a célula for calculada; chamar qualquer função das informações XLM diferente de **xlfCaller** resulta em um erro **xlretInvXlfn**. 
    
### <a name="registering-worksheet-functions-as-thread-safe"></a>Registro de funções de planilha como livres de threads

Desde o Excel 2007, o Excel pode fazer o recálculo de vários threads de pasta de trabalho. Isso significa que ele pode atribuir diferentes instâncias de uma função livre de threads a threads concorrentes para reavaliação. Desde o Excel 2007, a maioria das funções internas da planilha são livres de threads. Desde o Excel 2007, o Excel também permite que XLLs registrem funções de planilha como livres de threads. Para fazer isso, inclua um caractere **$** após o último código de parâmetro em _pxTypeText_. 
  
> [!NOTE]
> Apenas as funções de planilha podem ser declaradas como livres de threads. O Excel não considera livre de threads uma função equivalente de planilha de macro, para que você não possa acrescentar os caracteres **#** e **$** ao argumento _pxTypeText _. 
  
Se você registrou uma função como livre de threads, garanta que ela se comportará como tal, embora o Excel recuse toda chamada não livre de threads por meio da API C. Por exemplo, se uma função livre de threads tentar chamar **xlfGetCell**, a chamada falhará com o erro **xlretNotThreadSafe**. 
  
### <a name="registering-worksheet-functions-as-cluster-safe"></a>Registro de funções de planilha como livres de cluster

Desde o Excel 2010, o Excel pode descarregar chamadas de função para um provedor de cluster de cálculo designado. Confira mais informações em [Funções livres de cluster](cluster-safe-functions.md). Toda função de planilha XLL registrada como livre de cluster participará do descarregamento se um cluster estiver disponível. As funções livres de cluster são registradas por meio da inclusão do caractere **&amp;** após o último código de parâmetro no argumento _pxTypeText_. 
  
Se você tiver registrado uma função como livre de cluster, garanta que ela se comportará como tal. Confira mais informações em [Funções livres de cluster](cluster-safe-functions.md).
  
> [!NOTE]
> Apenas as funções de planilha podem ser declaradas como livres de cluster. O Excel não considera livre de cluster uma função equivalente de planilha de macro, para que você não possa acrescentar os caracteres **#** e **&amp;** ao argumento _pxTypeText _. As funções de planilha podem ser declaradas como livres de cluster e livres de threads ao mesmo tempo. Nesse caso, o Excel permitirá que essas funções participem do recálculo de vários threads quando a descarga de cluster estiver desabilitada. 
  
### <a name="category-names"></a>Nomes de categoria

Use as seguintes diretrizes para determinar em que categoria colocar as funções XLL.
  
- Se a função fizer algo que poderia ser feito pelo usuário como parte da sua interface de usuário do suplemento, coloque-a na categoria **Comandos**. 
    
- Se a função retornar informações sobre o estado do suplemento ou outras informações úteis, coloque-a na categoria **Informações**. 
    
- Um suplemento nunca deve adicionar funções ou comandos à categoria **Definido pelo Usuário**. Esta categoria é para uso exclusivo de usuários finais. 
    
A categoria é especificada usando o parâmetro _pxCategory_ para **xlfRegister**. Isso pode ser um número ou texto que corresponda a uma das categorias padrão embutidas em código ou o texto de uma nova categoria especificada pelo DLL. Se o texto fornecido já não existir, o Excel criará uma nova categoria com esse nome.
  
A tabela a seguir lista as categorias padrão que ficam visíveis quando você exibe a caixa de diálogo **Colar função** dentro de uma planilha. 
  
|**Número**|**Texto**|
|:-----|:-----|
|1  <br/> |Financeiro  <br/> |
|2  <br/> |Data e Hora  <br/> |
|3  <br/> |Matemática e Trigonometria  <br/> |
|4  <br/> |Texto  <br/> |
|5  <br/> |Lógica  <br/> |
|6  <br/> |Procura e Referência  <br/> |
|7  <br/> |Banco de dados  <br/> |
|8  <br/> |Estatística  <br/> |
|9  <br/> |Informações  <br/> |
|14  <br/> |Definido pelo Usuário  <br/> |
||Engenharia (a partir do Excel 2007)  <br/> |
||Cubo (a partir do Excel 2007)  <br/> |
   
Além disso, essas categorias também ficam visíveis quando você exibe a caixa de diálogo **Colar função** dentro de uma planilha de macro. 
  
|**Número**|**Texto**|
|:-----|:-----|
|10  <br/> |Comandos  <br/> |
|11  <br/> |DDE/Externo  <br/> |
|12  <br/> |Personalização  <br/> |
|13  <br/> |Controle de macro  <br/> |
   
### <a name="example"></a>Exemplo

Confira o código para a função **xlAutoOpen** em `\SAMPLES\GENERIC\GENERIC.C`.
  
## <a name="see-also"></a>Confira também

- [REGISTER.ID](xlfregisterid.md)
- [UNREGISTER](xlfunregister-form-1.md)
- [Funções XLM essenciais e úteis para a API C](essential-and-useful-c-api-xlm-functions.md)

