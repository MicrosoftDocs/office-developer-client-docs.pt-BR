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
ms.openlocfilehash: 2db55d6318cf02dd131d07b34841922e61605147
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432314"
---
# <a name="iconvertersession--iunknown"></a>IConverterSession : IUnknown

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Permite conversões entre objetos MIME e mensagens MAPI. Isso pode ser útil no transporte de mensagens pela Internet.
  
|||
|:-----|:-----|
|Provided by:  <br/> |CLSID_IConverterSession  <br/> |
|Identificador de interface:  <br/> |IID_IConverterSession  <br/> |
   
## <a name="vtable-order"></a>Vtable order

|||
|:-----|:-----|
|**[SetAdrBook](iconvertersession-setadrbook.md)** <br/> |Especifica um Address Book MAPI opcional que o conversor MAPI para MIME usa para resolver endereços ambíguos ao converter uma mensagem MAPI em um fluxo MIME.  <br/> |
|**[SetEncoding](iconvertersession-setencoding.md)** <br/> |Inicializa a codificação a ser usada durante a conversão.  <br/> |
| *Membro placeholder*  <br/> | *Sem suporte ou documentado.*  <br/> |
|**[MIMEToMAPI](iconvertersession-mimetomapi.md)** <br/> |Converte um fluxo MIME em uma mensagem MAPI.  <br/> |
|**[MAPIToMIMEStm](iconvertersession-mapitomimestm.md)** <br/> |Converte uma mensagem MAPI em um fluxo MIME.  <br/> |
| *Membro placeholder*  <br/> | *Sem suporte ou documentado.*  <br/> |
| *Membro placeholder*  <br/> | *Sem suporte ou documentado.*  <br/> |
| *Membro placeholder*  <br/> | *Sem suporte ou documentado.*  <br/> |
|**[SetTextWrapping](iconvertersession-settextwrapping.md)** <br/> |Define a largura da quebra de texto para um fluxo MIME que o conversor retorna em **MAPIToMIMEStm**.  <br/> |
|**[SetSaveFormat](iconvertersession-setsaveformat.md)** <br/> |Define o formato que o conversor retorna um fluxo MIME em **MAPIToMIMEStm**.  <br/> |
| *Membro placeholder*  <br/> | *Sem suporte ou documentado.*  <br/> |
|**[SetCharSet](iconvertersession-setcharset.md)** <br/> |Especifica um conjunto de caracteres opcional que o conversor MAPI para MIME usa ao converter uma mensagem MAPI em um fluxo MIME.  <br/> |
   
## <a name="remarks"></a>Comentários

Chame **SetEncoding antes** de usar **MAPIToMIMEStm** para executar a conversão. 
  
## <a name="see-also"></a>Confira também



[Sobre a API de conversão MAPI-MIME](about-the-mapi-mime-conversion-api.md)
  
[Constantes de MAPI](mapi-constants.md)

