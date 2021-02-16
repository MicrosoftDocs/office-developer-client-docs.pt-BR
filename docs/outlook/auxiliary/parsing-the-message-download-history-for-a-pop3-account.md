---
title: Analisar o histórico de download de mensagens de uma conta POP3
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 394e1430-04d6-4d61-be13-eb695309fa73
description: Este tópico descreve como a estrutura POP3 BLOB que representa o histórico de download da mensagem de uma conta POP3 e identifica mensagens baixadas ou excluídas nessa conta.
ms.openlocfilehash: 44a799f6b6fbe2a2841522c18405149a470b0236
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327754"
---
# <a name="parsing-the-message-download-history-for-a-pop3-account"></a>Analisar o histórico de download de mensagens de uma conta POP3

Este tópico descreve como a estrutura POP3 BLOB que representa o histórico de download da mensagem de uma conta POP3 e identifica mensagens baixadas ou excluídas nessa conta.

<a name="OL15Con_AuxRef_ParsingMsgsHistory_WhyParseHistory"> </a>

## <a name="why-parse-the-message-download-history"></a>Por que analisar o histórico de download da mensagem?

O provedor de protocolo POP (Post Office) para o Outlook permite aos usuários recuperarem e baixarem novas mensagens de email em seu dispositivo local e posteriormente sair ou excluir essas mensagens de email no servidor de email. Quando o cliente de email verifica se há novas mensagens baixar, deve ser capazes de identificar e baixar as novas mensagens para essa caixa de entrada. O cliente de email faz isso primeiramente usando o comando UIDL (lista de ID exclusivo) para obter um mapa de cada mensagem que já foi enviada para essa caixa de entrada para um identificador exclusivo (UID). O cliente também obtém o histórico de download de mensagem para mensagens baixadas ou excluídas na caixa de entrada desse cliente. Usando o mapa de mensagem UID e o histórico de download, o cliente pode identificar mensagens ausentes do histórico como novas e fazer o download em seguida.
  
Para obter histórico de download de mensagem para a caixa de entrada:
  
- Siga as etapas [localizar o histórico de download da mensagem para uma conta POP3](locating-the-message-download-history-for-a-pop3-account.md) para localizar a propriedade[PidTagAttachDataBinary](https://msdn.microsoft.com/library/3b0a8b28-863e-4b96-a4c0-fdb8f40555b9%28Office.15%29.aspx) que contém um objeto binário grande (BLOB) que representa o histórico de mensagem de uma conta POP3. 
    
- Leia este tópico que descreve a estrutura do BLOB e mostra um exemplo de BLOBs para identificar mensagens baixadas ou excluídas da caixa de entrada da conta POP3.

<a name="OL15Con_AuxRef_ParsingMsgsHistory_BLOBStructure"> </a>

## <a name="pop-blob-structure"></a>Estrutura de BLOB POP

Estrutura POP BLOBs, conforme descrito na tabela 1, comece com dois campos **versão** e **contagem** seguido pelo número de **contagem** das marcas de recurso, cada uma delas é terminada por caractere nulo. 
  
**Tabela 1. Estrutura de BLOBs que representa o histórico de download de mensagem de uma conta POP3**

|**Campo de BLOB**|**Tamanho**|**Descrição**|
|:-----|:-----|:-----|
|**Versão** <br/> |2 bytes  <br/> |Deve ser 3 (**PBLOB_VERSION_NUM**).  <br/> |
|**Contagem** <br/> |2 bytes  <br/> |O número das marcas de recurso neste BLOB.  <br/> |
|Marca de recursos  <br/> |Variável  <br/> |Terminada em 0 ou por caractere nulo ou UTF-8 cadeias de caracteres que codificam as marcas de recursos. O número de cadeias de caracteres terminada por caractere nulo deve corresponder com a **contagem**.  <br/> |
   
Cada marca de recurso especifica a operação que é aplicada a uma mensagem, alguns metadados de data e hora sobre a operação e também codifica o UID da mensagem. O formato de uma cadeia de marca de recursos funciona da seguinte forma e isso será explicado em detalhes na tabela 2. 
  
`Ocyyyymmddhhmmssuuu...`
  
**Tabela 2. Estrutura de uma marca de recursos**

|**Campo em uma marca de recursos**|**Tamanho**|**Descrição**|
|:-----|:-----|:-----|
| `O` <br/> |1 caractere  <br/> |Executar a operação na mensagem de email. O valor deve ser "+" ",", ou "&amp;", o que indica as operações obtenção bem-sucedida, excluir ou obter e excluir, respectivamente.  <br/> |
| `c` <br/> |1 caractere  <br/> |Parte do conteúdo da mensagem envolvido na operação. O valor deve ser "", "h" ou "b", que indica o conteúdo de nenhuma, cabeçalho ou corpo, respectivamente.  <br/> |
| `yyyy` <br/> |4 caracteres  <br/> |Os quatro dígitos do ano da operação.  <br/> |
| `MM` <br/> |2 caracteres  <br/> |Os dois dígitos do mês da operação.  <br/> |
| `dd` <br/> |2 caracteres  <br/> |Os dois dígitos do dia da operação.  <br/> |
| `hh` <br/> |2 caracteres  <br/> |Os dois dígitos da hora da operação.  <br/> |
| `mm` <br/> |2 caracteres  <br/> |Os dois dígitos do minuto da operação.  <br/> |
| `ss` <br/> |2 caracteres  <br/> |Os dois dígitos do segundo da operação.  <br/> |
| `uuu…` <br/> |Tamanho variável  <br/> |UID codificado de uma mensagem.  <br/> |

<a name="OL15Con_AuxRef_ParsingMsgsHistory_Example"> </a>

## <a name="example"></a>Exemplo

Tabela 1. Mostra um exemplo de BLOB que representa o histórico de download de mensagem de uma conta POP. 
  
**Figura 1. Exemplo de estrutura de BLOBs para download de histórico de mensagem de uma conta POP3**

![BLOB for messages download history of POP3 account](media/OL15Con_AuxRef_ParsingMsgsHistory_Blob.gif)
  
Com base na estrutura descrita na tabela 1 e na tabela 2, este BLOB representa o histórico de download de 23 mensagens de email.
  
Para analisar o UID bruto em cada marca de recurso, esteja ciente de que o UID segue este codificação: caracteres em UID são essencialmente caracteres alfanuméricos e cada caractere não alfanumérico é precedido pelos caracteres ASCII "$" (0x24). Então, os caracteres ASCII $2d representam os caracteres não-alfanuméricos ",". A figura 2 mostra um exemplo da primeira conversão UID bruta na marca de recursos 1 para a representação ASCII e depois a conversão de caracteres não alfanuméricos precedidos por "$" para produzir UID real:
  
`0BC535DB-EA63-11E1-A75C-00215AD7BB74`
  
**Figura 2. Converter o UID bruto em uma marca de recursos para a mensagem UID real**

![Converting raw UID in BLOB to actual message UID](media/OL15Con_AuxRef_ParsingMsgsHistory_BlobRscTag.gif)
  
Para interpretar a marca de recursos 1 nesse BLOB: a mensagem com UID `0BC535DB-EA63-11E1-A75C-00215AD7BB74` foi recuperada com êxito em 6 de setembro de 2012 às 13:11:38. 
  
Da mesma forma, você pode analisar as demais 22 marcas de recurso para aquele BLOB.
  
## <a name="see-also"></a>Confira também
<a name="OL15Con_AuxRef_ParsingMsgsHistory_AdditionalRsc"> </a>

- [Gerenciar o download de mensagens de contas POP3](managing-message-downloads-for-pop3-accounts.md)    
- [Localizar o histórico de download de mensagens de uma conta POP3](locating-the-message-download-history-for-a-pop3-account.md)    
- [Analise o histórico UIDL POP3](https://blogs.msdn.com/b/stephen_griffin/archive/2012/12/04/parsing-the-pop3-uidl-history.aspx)
    

