---
title: Propriedade canônica PidTagOriginatingMtaCertificate
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginatingMtaCertificate
api_type:
- COM
ms.assetid: f6b7ff0c-19a0-4cad-8868-c05397fcebf4
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7c5cfa8f80895896eab9af5ce1f249b9b06cf425
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769600"
---
# <a name="pidtagoriginatingmtacertificate-canonical-property"></a>Propriedade canônica PidTagOriginatingMtaCertificate

  
  
**Aplica-se a**: Outlook 
  
Contém um identificador para o agente de transferência de mensagem (MTA) que originou a mensagem.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_ORIGINATING_MTA_CERTIFICATE  <br/> |
|Identificador:  <br/> |0x0E25  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Servidor  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade, se definido, está disponível em mensagens enviadas na pasta Itens enviados.
  
Essa propriedade corresponde ao atributo x. 400 relatório-message.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições das propriedades listadas como propriedades associadas.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

