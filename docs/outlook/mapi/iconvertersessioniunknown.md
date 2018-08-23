---
title: IConverterSession IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IConverterSession
api_type:
- COM
ms.assetid: 24f7a14a-aa6f-4045-054b-4a7aefef25e4
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 316e17e7804e754eed4ee4fef27211fb5173d4bc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589641"
---
# <a name="iconvertersession--iunknown"></a>IConverterSession : IUnknown

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Permite conversões entre os objetos MIME e mensagens MAPI. Isso pode ser útil em transporte de mensagens pela Internet.
  
|||
|:-----|:-----|
|Provided by:  <br/> |CLSID_IConverterSession  <br/> |
|Identificador de interface:  <br/> |IID_IConverterSession  <br/> |
   
## <a name="vtable-order"></a>Ordem vtable

|||
|:-----|:-----|
|**[SetAdrBook](iconvertersession-setadrbook.md)** <br/> |Especifica um catálogo de endereços MAPI opcional que usa de MAPI conversor de MIME para resolver endereços ambíguos ao converter uma mensagem MAPI para um fluxo MIME.  <br/> |
|**[SetEncoding](iconvertersession-setencoding.md)** <br/> |Inicializa a codificação a ser usada durante a conversão.  <br/> |
| *Membro do espaço reservado*  <br/> | *Não tem suporte ou documentadas.*  <br/> |
|**[MIMEToMAPI](iconvertersession-mimetomapi.md)** <br/> |Converte um fluxo MIME em uma mensagem MAPI.  <br/> |
|**[MAPIToMIMEStm](iconvertersession-mapitomimestm.md)** <br/> |Converte uma mensagem MAPI em um fluxo MIME.  <br/> |
| *Membro do espaço reservado*  <br/> | *Não tem suporte ou documentadas.*  <br/> |
| *Membro do espaço reservado*  <br/> | *Não tem suporte ou documentadas.*  <br/> |
| *Membro do espaço reservado*  <br/> | *Não tem suporte ou documentadas.*  <br/> |
|**[SetTextWrapping](iconvertersession-settextwrapping.md)** <br/> |Define o largura de um fluxo MIME que o conversor retorna em **MAPIToMIMEStm**de quebra de texto.  <br/> |
|**[SetSaveFormat](iconvertersession-setsaveformat.md)** <br/> |Define o formato que o conversor retorna um fluxo MIME em **MAPIToMIMEStm**.  <br/> |
| *Membro do espaço reservado*  <br/> | *Não tem suporte ou documentadas.*  <br/> |
|**[SetCharSet](iconvertersession-setcharset.md)** <br/> |Especifica o que conjunto de um caractere opcional que MAPI conversor de MIME usa ao converter uma mensagem MAPI para um fluxo MIME.  <br/> |
   
## <a name="remarks"></a>Comentários

Chame **SetEncoding** antes de usar **MAPIToMIMEStm** para executar a conversão. 
  
## <a name="see-also"></a>Confira também



[Sobre a API de conversão MAPI-MIME](about-the-mapi-mime-conversion-api.md)
  
[Constantes MAPI](mapi-constants.md)

