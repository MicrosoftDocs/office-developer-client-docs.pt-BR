---
title: xlfRegister (Formulário 1)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfRegister
keywords:
- função xlfRegister [excel 2007]
localization_priority: Normal
ms.assetid: c730124c-1886-4a0f-8f06-79763025537d
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 4fb4e8656b4f27105a30764cdda020849a07645e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765472"
---
# <a name="xlfregister-form-1"></a>xlfRegister (Formulário 1)

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Pode ser chamado a partir de um comando DLL ou XLL próprio foi chamado pelo Microsoft Excel. Isso é igual a chamar **registrar** a partir de uma folha de macro do Excel XLM. 
  
**xlfRegister** pode ser chamado de duas formas: 
  
- xlfRegister (formulário 1): registra um único comando ou uma função.
    
- [xlfRegister (formulário 2)](xlfregister-form-2.md): cargas e ativa um XLL.
    
Chamado no formulário 1, essa função disponibiliza um comando ou uma função de DLL para Excel, define sua contagem de uso como 1 e retorna sua ID de registro, que pode ser usado para chamar a função posteriormente usando o [xlUDF](xludf.md) ou a função **xlfCall** . A identificação de registro também é usada para cancelar o registro a função usando [xlfUnregister (formulário 1)](xlfunregister-form-1.md). Se a função foi registrada, chamar **xlfRegister** novamente incrementa a contagem de seu uso. 
  
Esta forma da função também define um nome oculto, que é o argumento de texto de função, _pxFunctionText_, e que avalia para a ID do registro da função ou do comando. Quando você cancelar o registro a função, exclua esse nome usando o [xlfSetName](xlfsetname.md). Para obter mais informações, consulte [Problemas conhecidos no desenvolvimento de XLL do Excel](known-issues-in-excel-xll-development.md).
  
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
  
O nome da DLL que contém a função. Isso pode ser obtido chamando-se a função somente XLL [xlGetName](xlgetname.md) se a função registrada também estiver dentro da DLL atualmente em execução. 
  
_pxProcedure_ (**xltypeStr** ou **xltypeNum**)
  
Se uma cadeia de caracteres, o nome da função a ser chamada como ele aparece no código DLL. Se um número, o número ordinal exportar o número da função a ser chamada. Para manter a clareza, sempre use o formulário de cadeia de caracteres.
  
_pxTypeText_ (**xltypeStr**)
  
Uma cadeia de caracteres opcional que especifica os tipos dos argumentos para a função e o tipo do valor de retorno da função. Para obter mais informações, consulte a seção Comentários. Este argumento pode ser omitido para uma DLL autônomo (XLL) que inclui uma [função xlAutoRegister](xlautoregister-xlautoregister12.md) ou **xlAutoRegister12**. 
  
> [!NOTE]
> **xlAutoRegister12** só é suportado no Excel 2007. 
  
Se **xlfRegister** é chamado com este argumento ausente, Excel chama **xlAutoRegister** ou **xlAutoRegister12**, se qualquer um dos existe na DLL especificada, que deve registrar corretamente a função fornecendo essas informações.
  
_pxFunctionText_ (**xltypeStr**)
  
O nome da função como ela aparecerá no Assistente de função. Este argumento é opcional. Se ele for omitido, a função não está disponível no Assistente de função e só pode ser chamada usando a função de **chamada** usando a ID de registro de funções de uma folha de macro XLM. Portanto, para uso de planilha comum, você deve tratar este argumento conforme necessário. 
  
_pxArgumentText_ (**xltypeStr**)
  
Uma sequência de caracteres de texto opcional que descreve os argumentos para a função. O usuário vê isso no Assistente de função. Se ele for omitido, o Excel constrói básicas descrições de _pxTypeText_.
  
_pxMacroType_ (**xltypeNum** ou **xltypeInt**)
  
Um argumento opcional que indica o tipo de entrada XLL ponto. O valor padrão, se ele for omitido, é 1.
  
|||||
|:-----|:-----|:-----|:-----|
| _valor de pxMacroType_ <br/> |0  <br/> |1  <br/> |2  <br/> |
|Pode ser chamado a partir de uma planilha  <br/> |Sim  <br/> |Sim  <br/> |Não  <br/> |
|Pode ser chamado a partir de uma folha de macro  <br/> |Sim  <br/> |Sim  <br/> |Sim  <br/> |
|Pode ser chamado a partir de uma definição de nome definido  <br/> |Sim  <br/> |Sim  <br/> |Sim  <br/> |
|Pode ser chamado a partir de uma expressão de formato condicional  <br/> |Sim  <br/> |Sim  <br/> |Não  <br/> |
|Listado no Assistente de função para funções de planilha  <br/> |Não  <br/> |Sim  <br/> |Não  <br/> |
|Listado no Assistente de função para funções de folha de macro  <br/> |Não  <br/> |Sim  <br/> |Sim  <br/> |
   
Na prática, você deve usar 1 para funções de planilha, 1 para funções equivalentes de folha de macro (registrado como tipo **#**) que você deseja chamar a partir da planilha e 2 para comandos. 
  
> [!NOTE]
> Comandos XLL estão ocultos e não são exibidos nas caixas de diálogo para a execução de macros, embora seus nomes podem ser inseridos em qualquer lugar é necessário um nome de comando válido. 
  
_pxCategory_ (**xltypeStr** ou **xltypeNum**)
  
Um argumento opcional que permite que você especifique qual categoria de que a nova função ou o comando deve pertencer para. O Assistente de função divide funções por tipo (categoria). Você pode especificar um nome de categoria ou um número sequencial, onde o número é a posição na qual a categoria será exibida no Assistente de função. Para obter mais informações, consulte a seção "Nomes de categoria". Se ele for omitido, pressupõe-se a categoria definida pelo usuário.
  
_pxShortcutText_ (**xltypeStr**)
  
Uma sequência de um caractere, de maiusculas e minúsculas que especifica a chave de controle atribuída a este comando. Por exemplo, "A" atribui esse comando para CONTROL + SHIFT + A. Este argumento é opcional e é usado para comandos somente.
  
_pxHelpTopic_ (**xltypeStr**)
  
Uma referência de opcional para o arquivo de Ajuda (. chm ou. hlp) a ser exibido quando o usuário clica no botão Ajuda (quando sua função personalizada é exibida). Pode estar no formato `filepath!HelpContextID` ou `http://address/path_to_file_in_site!0`. Ambas as partes antes e depois o "!" são necessários.  *HelpContextID* não deve conter aspas simples e serão convertidos pelo Excel como um inteiro não assinado de 4 bytes de comprimento, em forma decimal. Ao usar o formulário de URL, o Excel abre somente o arquivo de ajuda referenciado. 
  
_pxFunctionHelp_ (**xltypeStr**)
  
Uma cadeia de caracteres opcional que descreve a sua função personalizada quando ele é selecionado no Assistente de função.
  
_pxArgumentHelp1_ (**xltypeStr**)
  
Opcional. A primeira das cadeias de caracteres que descrevem os argumentos personalizados da função quando a função é selecionada no Assistente de função. No Excel 2003 e versões anteriores, **xlfRegister** pode demorar, no máximo, 30 argumentos para que você possa fornecer essa ajuda para o primeiro 20 argumentos da função apenas. Iniciando no Excel 2007, **xlfRegister** pode demorar até 255 argumentos para que você possa fornecer essa ajuda para até 245 parâmetros de função. 
  
## <a name="property-valuereturn-value"></a>Valor de propriedade/Valor de retorno

Se o registro foi bem-sucedida, essa função retornará a identificação de registro da função (**xltypeNum**), que pode ser usada em chamadas **xlUDF** e **xlfUnregister** em uma DLL ou com **CHAMADAS** e **cancela o registro** em uma folha de macro XLM. Caso contrário, ele retornará um #VALUE! erro. 
  
## <a name="remarks"></a>Comentários

### <a name="data-types"></a>Tipos de dados

O argumento _pxTypeText_ Especifica o tipo de dados do valor de retorno e os tipos de dados de todos os argumentos para o DLL função ou recurso de código. O primeiro caractere da _pxTypeText_ Especifica o tipo de dados do valor de retorno. Os caracteres restantes indicam os tipos de dados de todos os argumentos. Por exemplo, uma função DLL que retorna um número de ponto flutuante e usa um número inteiro e um número de ponto flutuante como argumentos exigiria "BIB" para o argumento _pxTypeText_ . 
  
Os tipos de dados e estruturas usadas pelo Excel para trocar dados com XLLs são resumidas nas duas tabelas a seguir.
  
A primeira tabela lista os tipos suportados em todas as versões do Excel.
  
|**Tipo de dados**|**Passar por valor**|**Passar por ref (ponteiro)**|**Coment�rios**|
|:-----|:-----|:-----|:-----|
|Boolean  <br/> |A  <br/> |L  <br/> |Short [int] (0 = false ou 1 = true)  <br/> |
|double  <br/> |B  <br/> |E  <br/> ||
|char \*  <br/> ||C, F  <br/> |Cadeia de byte ASCII terminada em nulo  <br/> |
|unsigned char \*  <br/> ||D, G  <br/> |Cadeia de caracteres de byte ASCII contada  <br/> |
|curto n�o assinado [int]  <br/> |H  <br/> ||WORD de 16 bits  <br/> |
|[signed] short [int]  <br/> |I  <br/> |M  <br/> |inteiro assinado de 16 bits  <br/> |
|[signed long] int  <br/> |J  <br/> |N  <br/> |inteiro assinado de 32 bits  <br/> |
|FP  <br/> ||K  <br/> |Estrutura de matriz de ponto flutuante  <br/> |
|Array  <br/> ||O  <br/> |São passados três argumentos:<br/>-int curto não assinado\*<br/>-int curto não assinado\*<br/>-double]  <br/> |
|XLOPER  <br/> ||P  <br/> |Matrizes e valores de planilha de tipo variável  <br/> |
|||L  <br/> |Valores, matrizes e referências de intervalo  <br/> |
   
No Excel 2007, que os seguintes tipos de dados foram introduzidos dar suporte a Unicode longo e grades maiores strings.
  
|**Tipo de dados**|**Passar por valor**|**Passar por ref (ponteiro)**|**Coment�rios**|
|:-----|:-----|:-----|:-----|
|short não assinado\*  <br/> ||C%, F%  <br/> |Cadeia de toda a caracteres Unicode terminada em nulo  <br/> |
|short não assinado\*  <br/> ||D%, G%  <br/> |Cadeia de caracteres de toda a caracteres Unicode contada  <br/> |
|FP12  <br/> ||K%  <br/> |Estrutura de matriz de ponto flutuante de grade maior  <br/> |
|Array  <br/> ||O%  <br/> |São passados três argumentos:<br/>-assinado int \* / RW\*<br/>-assinado int \* / COL\*<br/>-double]  <br/> |
|XLOPER12  <br/> ||Q  <br/> |Matrizes e valores de planilha de tipo variável  <br/> |
|||U  <br/> |Valores, matrizes e referências de intervalo  <br/> |
   
Iniciando no Excel 2010, os seguintes dados foram introduzidos tipos:
  
|**Tipo de dados**|**Passar por valor**|**Passar por ref (ponteiro)**|**Coment�rios**|
|:-----|:-----|:-----|:-----|
|XLOPER12  <br/> ||X  <br/> |O identificador assíncrona é usado para rastrear uma chamada de função assíncrona pendente pelo Excel e XLL. A existência de tipo de parâmetro na cadeia de caracteres de tipo também designa a função como assíncrona. Para obter mais informações sobre funções assíncronas, consulte [Funções Asynchronous User-Defined](asynchronous-user-defined-functions.md).  <br/> |
   
Os tipos de cadeia de caracteres **F**, **F%**, **G** e **G%** s�o usados para os argumentos que s�o modificados no local. 
  
Ao trabalhar com os tipos de dados exibidos na tabela anterior, esteja ciente das seguintes opções:
  
- As declarações da linguagem C pressupõem que seu compilador usa valores duplos de 8 bytes, inteiros curtos de 2 bytes e inteiros longos de 4 bytes por padrão.
    
- Todas as funções em DLLs e recursos de código são chamadas usando **__stdcall** convenção de chamada. 
    
- Qualquer função que retorna um tipo de dados por referência, ou seja, que retorna um ponteiro para algo, com segurança pode retornar um ponteiro nulo. Excel interpreta um ponteiro nulo como um #NUM! erro.
    
## <a name="additional-data-type-information"></a>Informações de tipo de dados adicionais

Esta seção contém informações detalhadas sobre a **F**, **F**, **F %**, **G**, **G %**, **K**, **O**, **P**, **Q**, **R**e tipos de dados de **U** e outras informações sobre o pxTypeText _ _argumento. 
  
### <a name="e-data-type"></a>Tipo de dados E

Excel espera uma DLL usando o tipo de dados E passe ponteiros para números de ponto flutuante na pilha. Isso pode causar problemas com alguns idiomas (por exemplo, Borland C++) que o número a ser passado na pilha coprocessador emulador de espera. A solução alternativa é passar um ponteiro para o número na pilha coprocessador. O exemplo a seguir mostra como retornar um double da Borland C++.
  
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

### <a name="f-f-g-and-g-data-types"></a>F, F %, G e G % tipos de dados

Com o **F**, **F %**, **G**e **G %** tipos de dados, uma função pode modificar um buffer de cadeia de caracteres que é alocado pelo Excel. Se o código de tipo de valor de retorno é um desses tipos, o Excel ignora o valor retornado pela função. Em vez disso, o Excel procura na lista de argumentos da função para o primeiro tipo de dados correspondente (**F**, **F %**, **G**ou **G %**) e, em seguida, usa o conteúdo atual do buffer de sequência alocado como o valor de retorno. Todas as versões do Excel alocar de 256 bytes para **F** e cadeias de caracteres de ASCII **G** e iniciada no Excel 2007 65.536 bytes são alocados, suficientes para 32.768 caracteres Unicode, para **F %** e **% G** cadeias de caracteres Unicode. Lembre-se de que os buffers devem incluir um caractere de contagem (tipos **G** e **G %**) ou um caractere de finalização null (tipos **F** e **F %**), para que os comprimentos de cadeia de caracteres máximo real são 255 e 32,767. Cadeias de caracteres Unicode e, portanto, argumentos tipo **F %** e **% de G** , estão disponíveis somente por meio da API C no Excel. 
  
### <a name="k-and-k-data-types"></a>K e tipos de dados K %

Os tipos de dados **K** e **K %** usam ponteiros para as estruturas porte variável FP e FP12, respectivamente. Essas estruturas são definidas no XLLCALL. H. Estruturas de FP12 e, portanto, argumentos de tipo **K %** , só há suporte iniciando no Excel 2007. 
  
### <a name="o-and-o-data-types"></a>O e tipos de dados de % O

Os tipos de dados **O** e **O %** só pode ser usado para argumentos, não retornam valores, embora os valores podem ser retornados minha modificando um argumento de tipo **O** ou **O %** no lugar. Cada passa três itens: um ponteiro para o número de linhas em uma matriz, um ponteiro para o número de colunas em uma matriz e um ponteiro para uma matriz bidimensional de números de ponto flutuante. 
  
Para modificar uma matriz passada pelo ou O tipo de dados de % no lugar, você poderia usar "> O" ou "> O %" como o argumento _pxTypeText_ . Para obter mais informações sobre como modificar uma matriz, consulte a seção "Modificando no local: funções declaradas como nulas" neste tópico. 
  
O tipo de dados **O** foi criado para compatibilidade direta com DLLs do Fortran, que passam argumentos por referência. 
  
O **O %** é suportado iniciada no Excel 2007 e acomoda o maior número de linhas que suporta do Excel. 
  
### <a name="p-and-q-data-types"></a>Tipos de dados P e Q

Quando argumentos da função DLL são registrados como levando tipo **P** XLOPERs ou digite **Q** XLOPER12s, o Excel converte referências de célula única aos valores simples e referências de células múltiplos para matrizes ao preparar esses argumentos. Em outras palavras, tipos **P** e **Q** serão sempre chegam em sua função como um desses tipos: xltypeNil **xltypeNum**, **xltypeStr**, **xltypeBool**, **xltypeErr**, **xltypeMulti**, **xltypeMissing**ou ** **, mas não **xltypeRef** ou **xltypeSRef** porque eles são referenciados. **XLOPER12**s e, portanto, argumentos de tipo **Q** , só há suporte iniciando no Excel 2007. 
  
Se tipos **xltypeMissing** ou **xltypeNil** são usados para valores de retorno, eles são interpretados pelo Excel como zero numérico. **xltypeMissing** é passado quando o chamador omite um argumento. **xltypeNil** é passado quando o chamador passa uma referência a uma célula vazia. Quando um intervalo de células é convertido em um **xltypeMulti** a serem passados como tipo **P** ou **Q**, qualquer células vazias no intervalo são convertidas em elementos de matriz **xltypeNil** . Da mesma forma, os elementos ausentes em uma matriz literal são passados como **xltypeNil** elementos. 
  
### <a name="volatile-functions-and-recalculation"></a>Funções voláteis e recálculo

Em uma planilha, você pode fazer um DLL função ou recurso de código voláteis, para que ele recalcula toda vez que a planilha é recalculada. Para fazer isso, adicione um ponto de exclamação (!) após o último código de argumento no argumento _pxTypeText_ . 
  
> [!NOTE]
> Por padrão, as funções que assumem tipo **R** XLOPERs ou digite **U** XLOPER12s e que são registrados como macro planilha equivalentes (tipo **#**; consulte a próxima seção) são tratados como volátil no Excel. 
  
### <a name="functions-declared-as-void"></a>Funções declaradas como canceladas

Há dois casos que chamam para declarar uma função que não retornam void. Em ambos os casos, a função retornará seu resultado por outros meios.
  
#### <a name="modifying-in-place"></a>Modificando no local

Você pode usar um único dígito _n_ para o código de tipo de retorno no _pxTypeText_, onde _n_ é um número de 1 a 9. Isso instrui o Excel tirar o valor da variável no local apontado pelo argumento _n_th em _pxTypeText_ como o valor de retorno. Isso também é conhecido como modificar no local. O argumento _n_th deve ser um tipo de dados de passar por referência (C, D, F, F, F %, G, G %, K, K %, L, M, N, O, O %, P, Q, R ou U). O recurso de função ou código DLL também deve ser declarado com a palavra-chave **void** nas linguagens C/C++ (ou a palavra-chave **procedure** na linguagem Pascal). 
  
Por exemplo, uma função DLL que assume uma cadeia de caracteres terminada em nulo e dois ponteiros para inteiros como argumentos podem modificar a cadeia de caracteres no lugar. Use "1FMM" como o argumento _pxTypeText_ e declarar a função como nula. 
  
Versões anteriores do Excel usado **\>** no início do _pxTypeText_ para indicar que a função foi declarada como cancelada e que o primeiro argumento era a ser modificada no lugar — não havia nenhuma maneira de modificar qualquer argumento que não seja o primeiro. O **\>** é equivalente a _n_ = 1 no Excel versões atuais e este uso de **\>** em funções síncronas é suportado apenas para compatibilidade com versões anteriores. 
  
#### <a name="asynchronous-functions"></a>Funções assíncronas

Uma função assíncrona, indicada por meio de um parâmetro do tipo X em **pxTypeText**, não retorna seu resultado da chamada de função inicial. Em vez disso, você deve declarar uma função assíncrona como void e posteriormente o suplemento retorna o resultado por meio de um retorno de chamada. A função assíncrona deve ser registrada usando **\>** no início do **pxTypeText**. Em funções assíncronas, **\>** indica que a função é declarada como cancelada, mas não indica que o primeiro argumento é modificado no lugar. Para obter mais informações sobre funções assíncronas, consulte [Funções Asynchronous User-Defined](asynchronous-user-defined-functions.md). 

### <a name="registering-worksheet-functions-as-macro-sheet-equivalents-handling-uncalculated-cells"></a>Registrando as funções de planilha como equivalentes de folha de macro (lidar células não calculadas)

Colocar um **#** caractere após o último código de parâmetro no _pxTypeText_ concede a função as mesmas permissões chamando funções em uma folha de macro. Estas são as seguintes: 
  
- A função pode recuperar os valores das células que ainda não foram calculados nesse ciclo de recálculo.
    
- A função pode chamar qualquer uma das funções XLM informações (classe 2), por exemplo, **xlfGetCell**.
    
- Se o jogo da velha (#) não estiver presente: avaliando resultados uma célula não calculadas em um erro de **xlretUncalced** e a função atual é chamado novamente depois que a célula foi calculada; chamar qualquer função de informações de XLM que não seja **xlfCaller** resulta em erro **xlretInvXlfn** . 
    
### <a name="registering-worksheet-functions-as-thread-safe"></a>Registrando as funções de planilha como thread-safe

Iniciando no Excel 2007, Excel pode executar o recálculo de pasta de trabalho multithread. Isso significa que ele pode atribuir diferentes instâncias de uma função thread-safe segmentos simultâneos para reavaliação. Iniciando no Excel 2007, a maioria das funções de planilha internas é thread-safe. Iniciando no Excel 2007, Excel também permite XLLs registrar as funções de planilha como thread-safe. Para fazer isso, inclua um **$** caracteres após o último código de parâmetro no _pxTypeText_. 
  
> [!NOTE]
> Somente as funções de planilha podem ser declaradas como thread-safe. Excel não considera uma função equivalente de folha de macro para ser thread-safe, para que você não pode acrescentar ambos **#** e **$** caracteres para o argumento _pxTypeText_ . 
  
Se você registrou uma função como thread-safe, você deve garantir que ele se comporta em uma forma de thread-safe, embora Excel rejeita todas as chamadas não seguros thread por meio da API C. Por exemplo, se uma função thread-safe tenta chamar **xlfGetCell**, a chamada falhar com o erro **xlretNotThreadSafe** . 
  
### <a name="registering-worksheet-functions-as-cluster-safe"></a>Registrando as funções de planilha como cluster-safe

Iniciando no Excel 2010, Excel pode descarregamento de chamadas de função para um provedor de cluster de computação designada. Para obter mais informações, consulte [Funções de segurança de Cluster](cluster-safe-functions.md). Funções de planilha qualquer XLL registradas como cluster-safe participem no descarregamento se um cluster está disponível. Funções seguras do cluster registradas, incluindo o **&amp;** caracteres após o último código de parâmetro no argumento _pxTypeText_ . 
  
Se você registrou uma função como cluster-safe, certifique-se de que ele se comporta de forma segura de cluster. Para obter mais informações, consulte [Funções de segurança de Cluster](cluster-safe-functions.md).
  
> [!NOTE]
> Somente as funções de planilha podem ser declaradas como cluster-safe. Excel não considera uma função equivalente de folha de macro para ser seguras do cluster, de modo que você não pode acrescentar ambos **#** e **&amp;** caracteres para o argumento _pxTypeText_ . Funções de planilha podem ser declaradas como seguras do cluster e o thread-safe. Nesse caso, o Excel permitirá que essas funções participar de recálculo multithreaded quando o descarregamento de cluster está desativado. 
  
### <a name="category-names"></a>Nomes de categorias

Use as diretrizes a seguir para determinar qual categoria para colocar seu XLL funciona em.
  
- Se a função faz algo que poderia ser feita pelo usuário como parte da sua interface de usuário em suplementos, recomenda-se colocar a função na categoria **comandos** . 
    
- Se a função retorna informações sobre o estado do add-in ou quaisquer outras informações úteis, recomenda-se colocar a função na categoria **informações** . 
    
- Um suplemento deve nunca adicionar funções ou comandos à categoria **Definida pelo usuário** . Esta categoria é destinada a uso exclusivo dos usuários finais. 
    
A categoria é especificada usando o parâmetro _pxCategory_ para **xlfRegister**. Isso pode ser um número ou texto que corresponde a uma das categorias padrão codificadas ou o texto de uma nova categoria especificada pela DLL. Se o texto especificado não existir, o Excel criará uma nova categoria com esse nome.
  
A tabela a seguir lista as categorias padrão que estejam visíveis quando você exibe a caixa de diálogo **Função colar** de dentro de uma planilha. 
  
|**Número**|**Text**|
|:-----|:-----|
|1  <br/> |Financeira  <br/> |
|2  <br/> |Data &amp; tempo  <br/> |
|3  <br/> |Matemática &amp; trigonométrica  <br/> |
|4  <br/> |Texto  <br/> |
|5  <br/> |Lógica  <br/> |
|6  <br/> |Pesquisa &amp; referência  <br/> |
|7  <br/> |Banco de dados  <br/> |
|8  <br/> |Estatística  <br/> |
|9  <br/> |Informação  <br/> |
|14  <br/> |Definida pelo Usuário  <br/> |
||Engenharia (começando no Excel 2007)  <br/> |
||Cubo (começando no Excel 2007)  <br/> |
   
Além disso, essas categorias também estarão visíveis quando você exibe a caixa de diálogo **Função colar** de dentro de uma folha de macro. 
  
|**Número**|**Text**|
|:-----|:-----|
|10  <br/> |Comandos  <br/> |
|11  <br/> |DDE/Externa  <br/> |
|12  <br/> |Personalização  <br/> |
|13  <br/> |Controle de Macro  <br/> |
   
### <a name="example"></a>Exemplo

Ver o código para a função **xlAutoOpen** em `\SAMPLES\GENERIC\GENERIC.C`.
  
## <a name="see-also"></a>Confira também

- [REGISTER.ID](xlfregisterid.md)
- [CANCELAR O REGISTRO](xlfunregister-form-1.md)
- [Funções XLM essenciais e úteis para a API de C](essential-and-useful-c-api-xlm-functions.md)

