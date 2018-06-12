---
title: Fluxo de preenchimento automático
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: d4f380fa-2ed9-4c7c-9ef3-b32f8409f657
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 7fc1fae4ed648d59c273b20ced247f6d20e01a6f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766223"
---
# <a name="autocomplete-stream"></a>Fluxo de preenchimento automático

  
  
**Aplica-se a**: Outlook 
  
Além de saber como o Microsoft Outlook interage com o fluxo de preenchimento automático, você deve entender o formato binário do fluxo de AutoCompletar.
  
O fluxo de preenchimento automático é um conjunto de linhas de propriedade do destinatário que são salvos como um fluxo binário em conjunto com alguns metadados de escrituração contábil que é usado apenas pelo Microsoft Outlook 2013, o Microsoft Outlook 2010, o Microsoft Office Outlook 2007 e o Microsoft Outlook 2003. Os metadados são relevantes para interações do Outlook com o fluxo de AutoCompletar para que terceiros deve preservar o que há em cada bloco de metadados quando eles salvam um fluxo de AutoCompletar modificadas. Em outras palavras, terceiros deve modificar apenas a parte do conjunto de linhas do formato binário e preservar o que já foi em sobre os blocos de metadados do fluxo de AutoCompletar.
  
## <a name="stream-visualization"></a>Visualização de fluxo

O layout de alto nível do fluxo de AutoCompletar é da seguinte maneira:
  
Metadados (4 bytes)
  
Número da versão principal (4 bytes)
  
Número da versão secundária (4 bytes)
  
Número de linhas n (4 bytes)
  
Número de propriedades p da linha um (4 bytes)
  
Marca de propriedade de propriedade do 1 (4 bytes)
  
Propriedade 1 reservados da dados (4 bytes)
  
União de valor de propriedade do 1 (8 bytes)
  
Dados de valor de propriedade do 1 (0 ou variáveis bytes)
  
… (propriedade 2 por meio da propriedade P-1)
  
Marca de propriedade de propriedade do p (4 bytes)
  
Propriedade p reservados da dados (4 bytes)
  
União de valor de propriedade do p (8 bytes)
  
Dados de valor de propriedade do p (0 ou variáveis bytes)
  
Número de perguntas de propriedades na linha dois (4 bytes)
  
… (Propriedades de linha do dois)
  
… (linha 3 por meio de linha n-1)
  
Número de propriedades r na linha n (4 bytes)
  
… (linha n's propriedades)
  
Contagem de bytes de informações extras EI (4 bytes)
  
Informações extras (bytes EI)
  
Metadados (8 bytes)
  
Para obter um exemplo de uma estrutura de binário, consulte exemplo binário a [formato de arquivo do Outlook 2003/2007 NK2 e diretrizes de desenvolvedor.](http://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf)
  
## <a name="high-level-layout"></a>Layout de alto nível

O layout do fluxo de preenchimento automático de modo geral, é o seguinte:
  
|**Dados do valor**|**Número de Bytes**|
|:-----|:-----|
|Metadados  <br/> |4  <br/> |
|Número da versão principal  <br/> |4  <br/> |
|Número da versão secundária  <br/> |4  <br/> |
|Conjunto de linhas  <br/> |Variável  <br/> |
|Contagem de bytes de informações extras EI  <br/> |4  <br/> |
|Informações extras  <br/> |EI  <br/> |
|Metadados  <br/> |8  <br/> |
   
Ao ler este fluxo, se a versão principal é diferente de 12, então este fluxo deve não leitura ou gravação. A versão secundária atual do stream AutoCompletar é 0, que tem a contagem de bytes de informações extras definida como 0. Se a versão secundária é diferente do que 0, então haverá a informação extra que precisa ser lido quando o fluxo de leitura e preservadas durante a criação de fluxo de informações. A versão secundária também precisará ser preservada quando o fluxo de gravação. Se ambos esses não são preservados, instâncias do Outlook que escreveu a informação extra perderá os dados. 
  
> [!NOTE]
> Aplicativos não devem adicionar dados personalizados para o campo de informações extras ou altere a versão secundária encontram essa funcionalidade dar suporte a extensões do Outlook para o formato e extensões de terceiros não arbitrárias. 
  
## <a name="row-set-layout"></a>Layout do conjunto de linhas

O layout do conjunto de linhas é o seguinte: 
  
|**Dados do valor**|**Número de Bytes**|
|:-----|:-----|
|Número de linhas  <br/> |4  <br/> |
|Rows  <br/> |Variável  <br/> |
   
O número de linhas identifica quantas linhas são fornecidos na próxima parte da sequência fluxo binário.
  
## <a name="row-layout"></a>Layout de linha

Cada linha está no seguinte formato:
  
|**Dados do valor**|**Número de Bytes**|
|:-----|:-----|
|Número de propriedades  <br/> |4  <br/> |
|Propriedades  <br/> |Variável  <br/> |
   
O número de propriedades identifica quantos propriedades são fornecidos na próxima parte da sequência fluxo binário.
  
## <a name="property-layout"></a>Propriedade Layout

Cada propriedade está no seguinte formato:
  
|**Dados do valor**|**Número de Bytes**|
|:-----|:-----|
|Propriedade Tag  <br/> |4  <br/> |
|Dados reservado  <br/> |4  <br/> |
|União de valor de propriedade  <br/> ||
|Dados do valor  <br/> |0 ou variável (dependendo a marca prop)  <br/> |
   
## <a name="interpreting-the-property-value"></a>Interpretando o valor da propriedade

O valor de propriedade Union e os dados de valor são deve ser interpretado com base na marca de propriedade nos primeiros 4 bytes do bloco de propriedade. Marca essa propriedade está no mesmo formato apresentado uma marca de propriedade MAPI. Bits 0 a 15 da marca de propriedade são o tipo da propriedade. Bits de 16 a 31 são o identificador da propriedade. O tipo de propriedade determina como o restante da propriedade deve ser lido.
  
## <a name="static-value"></a>Valor estático

Algumas propriedades não têm nenhum dado de valor e tem somente os dados na União. Os seguintes tipos de propriedade (que vêm da marca de propriedade) devem interpretar os dados de propriedade de união de 8 bytes da seguinte maneira:
  
|**Tipo de prop**|**Interpretação de união de propriedade**|
|:-----|:-----|
|PT_I2  <br/> |int curto  <br/> |
|PT_LONG  <br/> |Longas  <br/> |
|PT_R4  <br/> |float  <br/> |
|PT_DOUBLE  <br/> |double  <br/> |
|PT_BOOLEAN  <br/> |int curto  <br/> |
|PT_SYSTIME  <br/> |FILETIME  <br/> |
|PT_I8  <br/> |LARGE_INTEGER  <br/> |
   
## <a name="dynamic-values"></a>Valores dinâmicos

Outras propriedades têm dados em um bloco de dados do valor após os primeiros 16 bytes que contêm a marca de propriedade, os dados reservados e o valor de propriedade Union. Diferentemente dos valores estáticos, os dados armazenados na União 8 bytes valor da propriedade são irrelevantes na leitura. Ao escrever, certifique-se de que você preencher essas 8 bytes com algo. No entanto, o conteúdo de 8 bytes não é importante. Tipo da marca de propriedade dinâmicos valores, determina como interpretar os dados do valor.
  
PT_STRING8 
  
|**Dados do valor**|**Número de Bytes**|
|:-----|:-----|
|Número de bytes n  <br/> |4  <br/> |
|Bytes a ser interpretada como uma cadeia de caracteres ANSI (inclui terminador nulo)  <br/> |m  <br/> |
   
PT_CLSID
  
|**Dados do valor**|**Número de Bytes**|
|:-----|:-----|
|Bytes deve ser interpretado como um GUID  <br/> |16  <br/> |
|||
   
PT_BINARY 
  
|**Dados do valor**|**Número de Bytes**|
|:-----|:-----|
|Número de bytes n  <br/> |4  <br/> |
|Bytes deve ser interpretado como uma matriz de bytes  <br/> |m  <br/> |
   
PT_ERROR
  
|**Dados do valor**|**Número de Bytes**|
|:-----|:-----|
|Número de bytes n  <br/> |4  <br/> |
|Bytes deve ser interpretado como uma matriz de bytes  <br/> |m  <br/> |
   
PT_MV_BINARY
  
|**Dados do valor**|**Número de Bytes**|
|:-----|:-----|
|Número de matrizes binários X  <br/> |4  <br/> |
|A execução de bytes que contém os X matrizes binários. Cada matriz deve ser interpretado exatamente como o byte PT_BINARY executar.  <br/> |Variável  <br/> |
   
PT_MV_STRING8 (Outlook 2007, Outlook 2010 e Outlook 2013)
  
|**Dados do valor**|**Número de Bytes**|
|:-----|:-----|
|Número de sequências de caracteres ANSI X  <br/> |4  <br/> |
|Uma sequência de bytes que contém as cadeias de caracteres ANSI X. Cada cadeia de caracteres deve ser interpretada exatamente como o byte PT_STRING8 executar.  <br/> |Variável  <br/> |
   
PT_MV_UNICODE (Outlook 2007, Outlook 2010, Outlook 2013)
  
|**Dados do valor**|**Número de Bytes**|
|:-----|:-----|
|Número de sequências de caracteres UNICODE X  <br/> |4  <br/> |
|Uma sequência de bytes que contém X UNICODE cadeias de caracteres. Cada cadeia de caracteres deve ser interpretada exatamente como o byte PT_UNICODE executar.  <br/> |Variável  <br/> |
   
## <a name="significant-properties"></a>Propriedades significativas

Conforme mencionado anteriormente neste tópico, os blocos de binários que representam propriedades têm marcas de propriedade que correspondem às propriedades nos destinatários de catálogo de endereços. Para propriedades que não estão listadas aqui, você pode consultar a descrição da propriedade em http://msdn.microsoft.com/en-us/library/cc433490(EXCHG.80).aspx.
  
|**Nome da propriedade**|**Propriedade Tag**|**Descrição (consulte o MSDN para obter mais informações)**|
|:-----|:-----|:-----|
|PR_NICK_NAME_W (não transmitidas nos destinatários, específicos de fluxo de AutoCompletar apenas)  <br/> |0x6001001f  <br/> |Esta propriedade deve ser o primeira em cada linha de destinatário. Funcionalmente, ela serve como um identificador de chave para a linha de destinatário.  <br/> |
|PR_ENTRYID  <br/> |0x0FFF0102  <br/> |O identificador de entrada de catálogo de endereços para o destinatário.  <br/> |
|PR_DISPLAY_NAME_W  <br/> |0x3001001F  <br/> |Nome para exibição do destinatário.  <br/> |
|PR_EMAIL_ADDRESS_W  <br/> |0x3003001F  <br/> |Endereço de email do destinatário (por exemplo, johndoe@contoso.com ou /o = Contoso/OU = Foo/cn = Recipients/cn = johndoe)  <br/> |
|PR_ADDRTYPE_W  <br/> |0x3002001F  <br/> |Tipo de endereço do destinatário (por exemplo, SMTP ou EX).  <br/> |
|PR_SEARCH_KEY  <br/> |0x300B0102  <br/> |Chave de pesquisa MAPI do destinatário.  <br/> |
|PR_SMTP_ADDRESS_W  <br/> |0x39FE001f  <br/> |Endereço de SMTP do destinatário.  <br/> |
|PR_DROPDOWN_DISPLAY_NAME_W (não transmitidas nos destinatários, específicos de fluxo de AutoCompletar apenas)  <br/> |0X6003001f  <br/> |A cadeia de caracteres de exibição que aparece na lista AutoCompletar.  <br/> |
|PR_NICK_NAME_WEIGHT (não transmitidas nos destinatários, específicos de fluxo de AutoCompletar apenas)  <br/> |0x60040003  <br/> |A espessura dessa entrada de AutoCompletar. O peso é usado para determinar em qual ordem de AutoCompletar ocorrer entradas na lista AutoCompletar de correspondência. Entradas com peso maior mostrará antes de entradas com peso mais baixo. A lista completa de AutoCompletar é classificada por esta propriedade. O peso periodicamente diminui ao longo do tempo e aumenta quando o usuário envia um email para o destinatário. Consulte a descrição neste tópico para obter mais informações sobre essa propriedade.  <br/> |
   
PR_NICK_NAME_WEIGHT
  
O conjunto de linhas no stream AutoCompletar é classificado em ordem decrescente pela propriedade PR_NICK_NAME_WEIGHT e o fluxo de AutoCompletar sempre deve preservar essa característica classificada. Portanto, quaisquer alterações para espessura da linha um também devem assegurar que a posição da linha mantém a ordem de classificação do conjunto completo de linhas. Quaisquer adições para o conjunto de linhas devem ser inseridas na posição correta para manter a ordem de classificação.
  
O valor mínimo desse peso é 0x1 e o valor máximo é LONG_MAX. Todos os outros valores para o peso são considerados inválidos.
  
Quando o Outlook 2007 envia um email para ou resolve um destinatário, ele será aumentado peso do destinatário que em 0x2000.
  

