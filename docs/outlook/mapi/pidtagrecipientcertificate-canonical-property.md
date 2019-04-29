---
title: Propriedade canônica PidTagRecipientCertificate
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientCertificate
api_type:
- COM
ms.assetid: 7c5c749e-5463-4935-85b5-32219d06f782
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: c659b77767fddc4c783732082c2eb65c68af8dbf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431663"
---
# <a name="pidtagrecipientcertificate-canonical-property"></a>Propriedade canônica PidTagRecipientCertificate

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém o certificado ASN de um destinatário de mensagem para uso em um relatório.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_RECIPIENT_CERTIFICATE  <br/> |
|Identificador:  <br/> |0x0C13  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Destinatário MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Esta propriedade é uma cópia da propriedade **PR_USER_CERTIFICATE** ([PidTagUserCertificate](pidtagusercertificate-canonical-property.md)) do destinatário para uso em um relatório. Ele pode ser usado para provar ao originador de que o destinatário realmente recebeu a mensagem, o que um relatório de entrega não necessariamente indica.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs. h
  
> Fornece definições de tipo de dados.
    
Mapitags. h
  
> Contém definições de propriedades listadas como propriedades associadas.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

