---
title: Propriedade canônica PidTagMailPermission
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMailPermission
api_type:
- HeaderDef
ms.assetid: f8270ef2-56d4-4b47-bdda-a39c966bbcba
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: fb0b66cbf0de1ac351bb2026a48e0154de779206
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571189"
---
# <a name="pidtagmailpermission-canonical-property"></a>Propriedade canônica PidTagMailPermission

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Conterá TRUE se o usuário de mensagens tem permissão para enviar e receber mensagens. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_MAIL_PERMISSION  <br/> |
|Identificador:  <br/> |0x3A0E  <br/> |
|Tipo de dados:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |Endereço  <br/> |
   
## <a name="remarks"></a>Comentários

Se essa propriedade não estiver definida, MAPI a tratará como tendo um valor TRUE. 
  
Defina essa propriedade como FALSE em um diretório corporativo, onde algumas das entradas não são habilitados para email. 
  
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

