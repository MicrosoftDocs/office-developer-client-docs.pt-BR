---
title: Fluxo de preenchimento automático
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: d4f380fa-2ed9-4c7c-9ef3-b32f8409f657
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: aadfba3e2674c35019a2e5f3eb374fbed1ad2a75
ms.sourcegitcommit: 0419850d5c1b3439d9da59070201fb4952ca5d07
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/28/2020
ms.locfileid: "49734221"
---
# <a name="autocomplete-stream"></a>Fluxo de preenchimento automático

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Além de saber como o Microsoft Outlook interage com o fluxo de preenchimento automático, você também deve entender formato binário dele.
  
O fluxo de preenchimento automático é um conjunto de linhas de propriedade de destinatário salvo como um fluxo de binário com alguns metadados contábeis usados apenas pelo Microsoft Outlook 2013, o Microsoft Outlook 2010, o Microsoft Office Outlook 2007 e o Microsoft Outlook 2003. Os metadados são relevantes para as interações do Outlook com o fluxo de preenchimento automático, assim terceiros devem manter o que está em cada bloco de metadados quando salvam um fluxo de preenchimento automático modificado. Em outras palavras, terceiros devem modificar apenas a parte do conjunto de linhas do formato binário e preservar o que já estava nos blocos de metadados do fluxo de preenchimento automático.
  
## <a name="stream-visualization"></a>Visualização de Fluxo

O layout de alto nível do fluxo de preenchimento automático é o seguinte:
  
Metadados (4 bytes)
  
Número da Versão Principal (4 bytes)
  
Número da Versão Secundária (4 bytes)
  
Número de linhas n (4 bytes)
  
Número de propriedades p na linha um (4 bytes)
  
Marca da propriedade 1 (4 bytes)
  
Dados reservados da propriedade 1 (4 bytes)
  
União de valor da propriedade 1 (8 bytes)
  
Dados de valor da propriedade 1 (0 byte ou bytes variáveis)
  
… (da propriedade 2 à propriedade P-1)
  
Marca da propriedade p (4 bytes)
  
Dados reservados da propriedade p (4 bytes)
  
União de valor da propriedade p (8 bytes)
  
Dados de valor da propriedade p (0 byte ou bytes variáveis)
  
Número de propriedades q na linha dois (4 bytes)
  
… (propriedades da linha dois)
  
… (da linha 3 à linha n-1)
  
Número de propriedades r na linha n (4 bytes)
  
… (propriedades da linha n)
  
EI de contagem de bytes de informações extras (4 bytes)
  
Informações extras (bytes EI)
  
Metadados (8 bytes)
  
Para ver um exemplo de estrutura binária, confira o Exemplo Binário nas [Diretrizes para Desenvolvedor e Formato de Arquivo do Outlook 2003/2007 NK2.](https://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf)
  
## <a name="high-level-layout"></a>Layout de Alto Nível

Em geral, o layout do fluxo de preenchimento automático é o seguinte:
  
|**Dados do Valor**|**Número de Bytes**|
|:-----|:-----|
|Metadados  <br/> |4   <br/> |
|Número da Versão Principal  <br/> |4   <br/> |
|Número da Versão Secundária  <br/> |4   <br/> |
|Conjunto de linhas  <br/> |Variável  <br/> |
|EI de contagem de bytes de informações extras  <br/> |4   <br/> |
|Informações extras  <br/> |EI  <br/> |
|Metadados  <br/> |8   <br/> |
   
Ao ler este fluxo, se a versão principal for diferente da 12, então ele não deverá ser lido nem gravado. A versão secundária atual do fluxo de preenchimento automático é 0, que tem a contagem de Bytes de Informações Extras definida como 0. Se a versão secundária for diferente de 0, então as informações extras apresentarão informações que precisam ser lidas na leitura do fluxo e preservadas na gravação do fluxo. A versão secundária também deverá ser preservada ao gravar o fluxo. Se ambas não forem preservadas, as instâncias do Outlook que gravarem informações extras perderão os dados. 
  
> [!NOTE]
> Aplicativos não devem adicionar dados personalizados ao campo Informações Extras nem alterar a versão secundária, já que esta funcionalidade existe para dar suporte ao formato de extensões do Outlook e a extensões não arbitrárias de terceiros. 
  
## <a name="row-set-layout"></a>Layout de conjunto de linhas

O layout do conjunto de linhas é o seguinte: 
  
|**Dados do Valor**|**Número de Bytes**|
|:-----|:-----|
|Número de linhas  <br/> |4   <br/> |
|Linhas  <br/> |Variável  <br/> |
   
O número de linhas identifica quantas linhas existem na próxima parte da sequência de fluxo binário.
  
## <a name="row-layout"></a>Layout de Linha

Cada linha tem o seguinte formato:
  
|**Dados do Valor**|**Número de Bytes**|
|:-----|:-----|
|Número de Propriedades  <br/> |4   <br/> |
|Propriedades  <br/> |Variável  <br/> |
   
O número de propriedades identifica quantas propriedades existem na próxima parte da sequência de fluxo binário.
  
## <a name="property-layout"></a>Layout de Propriedade

Cada propriedade tem o seguinte formato:
  
|**Dados do Valor**|**Número de Bytes**|
|:-----|:-----|
|Marca de Propriedade  <br/> |4   <br/> |
|Dados Reservados  <br/> |4   <br/> |
|União do Valor da Propriedade  <br/> ||
|Dados do Valor  <br/> |0 ou variável (dependendo da marca propr)  <br/> |
   
## <a name="interpreting-the-property-value"></a>Interpretar o Valor da Propriedade

A União do Valor da Propriedade e os Dados de Valor são interpretados com base na marca de propriedade dos primeiros 4 bytes do bloco de propriedade. Essa marca de propriedade está no mesmo formato de uma marca de propriedade MAPI. Os bits de 0 a 15 da marca propriedade indicam o tipo da propriedade. Os bits de 16 a 31 são o identificador da propriedade. O tipo de propriedade determina como o restante da propriedade deve ser lido.
  
## <a name="static-value"></a>Valor Estático

Algumas propriedades não têm Dados de Valor e só têm dados na união. Os seguintes tipos de propriedades (procedentes da Marca da Propriedade) devem interpretar os dados da União de Propriedade de 8 bytes da seguinte forma:
  
|**Tipo de Propr**|**Interpretação da União da Propriedade**|
|:-----|:-----|
|PT_I2  <br/> |short int  <br/> |
|PT_LONG  <br/> |long  <br/> |
|PT_ERROR  <br/> |long  <br/> |
|PT_R4  <br/> |float  <br/> |
|PT_DOUBLE  <br/> |double  <br/> |
|PT_BOOLEAN  <br/> |short int  <br/> |
|PT_SYSTIME  <br/> |FILETIME  <br/> |
|PT_I8  <br/> |LARGE_INTEGER  <br/> |
   
## <a name="dynamic-values"></a>Valores Dinâmicos

Outras propriedades têm dados em um bloco de Valor de Dados após os primeiros 16 bytes que contêm a Marca de Propriedade, os Dados Reservados e a União de Valor da Propriedade. Ao contrário dos valores estáticos, os dados armazenados na União de Valor da Propriedade 8 bytes são irrelevantes para a leitura. Ao gravar, certifique-se de preencher estes 8 bytes com algo. No entanto, o conteúdo desses 8 bytes não é importante. Nos valores dinâmicos, o tipo da marca de propriedade determina como interpretar os Dados de Valor.
  
PT_STRING8 
  
|**Dados do Valor**|**Número de Bytes**|
|:-----|:-----|
|Número de bytes n  <br/> |4   <br/> |
|Bytes a interpretar como uma cadeia de caracteres ANSI (inclui um terminador NULL)  <br/> |n  <br/> |
   
PT_CLSID
  
|**Dados do Valor**|**Número de Bytes**|
|:-----|:-----|
|Bytes a interpretar como um GUID  <br/> |16   <br/> |
|||
   
PT_BINARY 
  
|**Dados do Valor**|**Número de Bytes**|
|:-----|:-----|
|Número de bytes n  <br/> |4   <br/> |
|Bytes a serem interpretados como uma matriz de byte  <br/> |n  <br/> |
   
PT_MV_BINARY
  
|**Dados do Valor**|**Número de Bytes**|
|:-----|:-----|
|Número de matrizes binárias X  <br/> |4   <br/> |
|Uma execução de bytes com X matrizes binárias. Cada matriz deve ser interpretada exatamente como a execução de byte PT_BINARY.  <br/> |Variável  <br/> |
   
PT_MV_STRING8 (Outlook 2007, Outlook 2010, and Outlook 2013)
  
|**Dados do Valor**|**Número de Bytes**|
|:-----|:-----|
|Número de cadeias de caracteres ANSI X  <br/> |4   <br/> |
|Uma execução de bytes com X cadeias de caracteres ANSI. Cada cadeia de caracteres deve ser interpretada exatamente como a execução de byte PT_STRING8.  <br/> |Variável  <br/> |
   
PT_MV_UNICODE (Outlook 2007, Outlook 2010, Outlook 2013)
  
|**Dados do Valor**|**Número de Bytes**|
|:-----|:-----|
|Número de cadeias de caracteres UNICODE X  <br/> |4   <br/> |
|Uma execução de bytes que contém X cadeias de caracteres UNICODE. Cada cadeia de caracteres deve ser interpretada exatamente como a execução de byte PT_UNICODE.  <br/> |Variável  <br/> |
   
## <a name="significant-properties"></a>Propriedades significativas

Como mencionado anteriormente neste tópico, os blocos binários que representam propriedades têm marcas de propriedade que correspondem às propriedades nos destinatários de catálogo de endereços. Para as propriedades que não estão listadas aqui, você pode pesquisar a descrição da propriedade na https://msdn.microsoft.com/library/cc433490(EXCHG.80).aspx.
  
|**Nome da propriedade**|**Marca de Propriedade**|**Descrição (confira MSDN para saber mais)**|
|:-----|:-----|:-----|
|PR_NICK_NAME_W (não transmitida aos destinatários, específica apenas para o fluxo de preenchimento automático)  <br/> |0x6001001f  <br/> |Essa propriedade deve ser a primeira em cada linha de destinatário. Serve funcionalmente como um importante identificador para a linha de destinatário.  <br/> |
|PR_ENTRYID  <br/> |0x0FFF0102  <br/> |O identificador de entrada de catálogo de endereço do destinatário.  <br/> |
|PR_DISPLAY_NAME_W  <br/> |0x3001001F  <br/> |O nome de exibição do destinatário.  <br/> |
|PR_EMAIL_ADDRESS_W  <br/> |0x3003001F  <br/> |O endereço de email do destinatário (por exemplo, joaosilva@contoso.com ou /o=Contoso/OU=Foo/cn=Recipients/cn=joaosilva)  <br/> |
|PR_ADDRTYPE_W  <br/> |0x3002001F  <br/> |O tipo de endereço do destinatário (por exemplo, SMTP ou EX).  <br/> |
|PR_SEARCH_KEY  <br/> |0x300B0102  <br/> |A chave de pesquisa MAPI do destinatário.  <br/> |
|PR_SMTP_ADDRESS_W  <br/> |0x39FE001f  <br/> |O endereço SMTP do destinatário.  <br/> |
|PR_DROPDOWN_DISPLAY_NAME_W (não transmitida aos destinatários, específica apenas para o fluxo de preenchimento automático)  <br/> |0X6003001f  <br/> |A cadeia de caracteres de exibição exibida na lista de preenchimento automático.  <br/> |
|PR_NICK_NAME_WEIGHT (não transmitida aos destinatários, específica apenas para o fluxo de preenchimento automático)  <br/> |0x60040003  <br/> |O peso desta entrada de preenchimento automático. O peso é usado para determinar em que ordem ocorrem as entradas de preenchimento automático ao fazer a correspondência da lista preenchimento automático. Entradas com maior peso são exibidas antes de entradas com peso inferior. A lista completa de preenchimento automático é classificada por esta propriedade. O peso periodicamente diminui ao longo do tempo e aumenta quando o usuário envia um email para esse destinatário. Confira a descrição neste tópico para saber mais sobre essa propriedade.  <br/> |
   
PR_NICK_NAME_WEIGHT
  
O conjunto de linhas no fluxo de preenchimento automático é classificado em ordem decrescente pela propriedade PR_NICK_NAME_WEIGHT, e o fluxo de preenchimento automático sempre deve preservar esse característica de classificação. Portanto, alterações ao peso da linha também devem garantir que a posição da linha mantém a ordem de classificação do conjunto completo de linhas. Os acréscimos ao conjunto de linhas devem ser inseridos na posição correta para manter a ordem de classificação.
  
O valor mínimo deste peso é de 0x1 e o valor máximo é LONG_MAX. Outros valores de peso são considerados inválidos.
  
Quando o Outlook 2007 envia um email ou resolve um destinatário, ele aumenta o peso do destinatário em 0x2000.
  

