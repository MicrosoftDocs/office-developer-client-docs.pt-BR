---
title: Analisar o histórico de download de mensagens de uma conta POP3
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 394e1430-04d6-4d61-be13-eb695309fa73
description: Este tópico descreve a estrutura do BLOB POP3 que representa o histórico de download de mensagens de uma conta POP3, para identificar as mensagens que foram baixadas ou excluídas dessa conta.
ms.openlocfilehash: ffed3178e4e8b45f17fc335575a7febd77d40902
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766041"
---
# <a name="parsing-the-message-download-history-for-a-pop3-account"></a>Analisar o histórico de download de mensagens de uma conta POP3

Este tópico descreve a estrutura do BLOB POP3 que representa o histórico de download de mensagens de uma conta POP3, para identificar as mensagens que foram baixadas ou excluídas dessa conta.

<a name="OL15Con_AuxRef_ParsingMsgsHistory_WhyParseHistory"> </a>

## <a name="why-parse-the-message-download-history"></a>Por que analisar o histórico de download de mensagens?

O provedor de Post Office Protocol (POP) para o Outlook permite que os usuários para recuperar e baixar novas mensagens de email no seu dispositivo local e subsequentemente deixar ou excluir essas mensagens de email no servidor de email. Quando o cliente de email verifica novas mensagens baixar, ele deve ser capaz de identificar e baixe somente as novas mensagens para essa caixa de entrada. O cliente de email faz isso usando primeiro o comando UIDL (ID exclusiva listando) para obter um mapa de cada mensagem que nunca foi entregue para essa caixa de entrada para um identificador exclusivo (UID). O cliente também obtém o histórico de download da mensagem para mensagens que foram baixadas ou excluídas da caixa de entrada em que o cliente. Usando o mapa UID da mensagem e o histórico de download, o cliente pode, em seguida, identifique essas mensagens ausentes do histórico de como novo e, portanto, deve ser baixado.
  
Para obter as mensagens de histórico de download para uma caixa de entrada:
  
- Siga as etapas em [localizar a mensagem baixar o histórico de uma conta POP3](locating-the-message-download-history-for-a-pop3-account.md) para localizar a propriedade [PidTagAttachDataBinary](http://msdn.microsoft.com/library/3b0a8b28-863e-4b96-a4c0-fdb8f40555b9%28Office.15%29.aspx) , que contém um objeto binário grande (BLOB) que representa o histórico de mensagens para uma conta POP3. 
    
- Leia este tópico, que descreve a estrutura do BLOB e mostra um exemplo BLOB para identificar mensagens que foram baixadas ou excluídas da caixa de entrada da conta POP3.

<a name="OL15Con_AuxRef_ParsingMsgsHistory_BLOBStructure"> </a>

## <a name="pop-blob-structure"></a>Estrutura de BLOB POP

A estrutura de BLOB POP, conforme descrito na tabela 1, começa com dois campos, **versão** e **contagem**, seguido por um número de **contagem** de marcas de recurso, cada um deles é terminada em nulo. 
  
**Tabela 1. Estrutura do BLOB que representa a mensagem baixar o histórico de uma conta POP3**

|**Campo no BLOB**|**Size**|**Descrição**|
|:-----|:-----|:-----|
|**Versão** <br/> |2 bytes  <br/> |Deve ser 3 (**PBLOB_VERSION_NUM**).  <br/> |
|**Count** <br/> |2 bytes  <br/> |O número de marcas de recurso neste BLOB.  <br/> |
|Marca de recurso  <br/> |Variável  <br/> |0 ou mais terminada em nulo UTF-8 cadeias de caracteres que codificar as marcas de recurso. O número de sequências de caracteres terminada em nulo deve corresponder a **contagem**.  <br/> |
   
Cada marca de recurso Especifica a operação que será aplicada a uma mensagem, alguns metadados de data / hora sobre a operação e codifica o UID da mensagem. O formato de uma cadeia de caracteres de marca de recurso é decomposto da seguinte maneira e é ainda mais explicado na tabela 2. 
  
`Ocyyyymmddhhmmssuuu...`
  
**Tabela 2. Estrutura de uma marca de recurso**

|**Campo em uma marca de recurso**|**Size**|**Descrição**|
|:-----|:-----|:-----|
| `O` <br/> |1 caractere  <br/> |A operação é executada na mensagem de email. O valor deve ser "+", "-", ou "&amp;", que indica uma get bem-sucedida, excluir ou operação get-e-delete, respectivamente.  <br/> |
| `c` <br/> |1 caractere  <br/> |A parte do conteúdo da mensagem envolvido na operação. O valor deve ser "", "h" ou "b", que indica o conteúdo de nenhum, cabeçalho ou corpo, respectivamente.  <br/> |
| `yyyy` <br/> |4 caracteres  <br/> |O ano com quatro dígitos da operação.  <br/> |
| `MM` <br/> |2 caracteres  <br/> |O mês com dois dígitos da operação.  <br/> |
| `dd` <br/> |2 caracteres  <br/> |O dia de dois dígitos da operação.  <br/> |
| `hh` <br/> |2 caracteres  <br/> |A hora de dois dígitos da operação.  <br/> |
| `mm` <br/> |2 caracteres  <br/> |O minuto de dois dígitos da operação.  <br/> |
| `ss` <br/> |2 caracteres  <br/> |O segundo com dois dígitos da operação.  <br/> |
| `uuu…` <br/> |Comprimento variável  <br/> |O UID codificado de uma mensagem.  <br/> |

<a name="OL15Con_AuxRef_ParsingMsgsHistory_Example"> </a>

## <a name="example"></a>Exemplo

A Figura 1 mostra um exemplo de um BLOB que representa o histórico de download de mensagens de uma conta POP. 
  
**Figura 1. Estrutura de BLOB de exemplo para a mensagem de baixar o histórico de uma conta POP3**

![BLOB for messages download history of POP3 account](media/OL15Con_AuxRef_ParsingMsgsHistory_Blob.gif)
  
Com base na estrutura descrita na tabela 1 e a tabela 2, esse BLOB representa o histórico de download, 23 de mensagens de email.
  
Para analisar o UID bruto na marca de cada recurso, esteja ciente de que o UID segue esta codificação: caracteres em um UID são principalmente caracteres alfanuméricos, e cada caractere não-alfanuméricos precedido pelo caractere ASCII "$" (0x24). Para que o ASCII caracteres $2d representam o não alfanuméricos caractere "-". A Figura 2 mostra um exemplo de como converter primeiro o UID bruto na marca de recurso 1 à representação ASCII, em seguida, convertendo qualquer caractere não-alfanuméricos precedido por "$" para produzir o UID real:
  
`0BC535DB-EA63-11E1-A75C-00215AD7BB74`
  
**Figura 2. Convertendo o UID bruto em uma marca de recurso para a mensagem real UID**

![Converting raw UID in BLOB to actual message UID](media/OL15Con_AuxRef_ParsingMsgsHistory_BlobRscTag.gif)
  
Interpretar a marca de recurso 1 neste BLOB: a mensagem com o UID `0BC535DB-EA63-11E1-A75C-00215AD7BB74` foi recuperado com êxito em 6 de setembro de 2012, em 13:11:38. 
  
Da mesma forma, você pode analisar as demais marcas de 22 de recurso para esse BLOB.
  
## <a name="see-also"></a>Confira também
<a name="OL15Con_AuxRef_ParsingMsgsHistory_AdditionalRsc"> </a>

- [Gerenciar o download de mensagens de contas POP3](managing-message-downloads-for-pop3-accounts.md)    
- [Localizar o histórico de download de mensagens de uma conta POP3](locating-the-message-download-history-for-a-pop3-account.md)    
- [Analisar o histórico UIDL POP3](http://blogs.msdn.com/b/stephen_griffin/archive/2012/12/04/parsing-the-pop3-uidl-history.aspx)
    

