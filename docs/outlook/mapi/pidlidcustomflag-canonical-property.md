---
title: Propriedade canônica PidLidCustomFlag
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidCustomFlag
api_type:
- COM
ms.assetid: bfb7fd1e-774f-9a2f-fbbe-ba7f68ed8663
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 9a131c633b8dcf9b0e5070f01de8fcab90a18ade
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384196"
---
# <a name="pidlidcustomflag-canonical-property"></a>Propriedade canônica PidLidCustomFlag

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Uma máscara de bits que especifica como uma mensagem é personalizada, por exemplo, salvo com propriedades personalizadas.
  
## 

|||
|:-----|:-----|
|Propriedades associadas:  <br/> |dispidCustomFlag  <br/> |
|ID de longo (LID):  <br/> |0x00008251  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
   
## <a name="remarks"></a>Comentários

Para recuperar o valor dessa propriedade, primeiro use **[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)** para obter a marca de propriedade e especifique nesta marca de propriedade em **[IMAPIProp::GetProps](imapiprop-getprops.md)** para obter o valor. 
  
Sinalizadores possíveis são:
  
****

|**Constante**|**Valor**|
|:-----|:-----|
|INSP_ONEOFFFLAGS  <br/> |0x0D000000  <br/> |
|INSP_PROPDEFINITION  <br/> |0x02000000  <br/> |
   
Ao chamar **IMAPIProp::GetIDsFromNames**, especifique os seguintes valores para a estrutura **[MAPINAMEID](mapinameid.md)** apontado pelo parâmetro de entrada *lppPropNames* . 
  
****

|**Membro**|**Valor**|
|:-----|:-----|
|lpGuid:  <br/> |PSETID_Common  <br/> |
|ulKind:  <br/> |MNID_ID  <br/> |
|Kind.lID:  <br/> |dispidCustomFlag  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece as definições do conjunto de propriedades.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições das propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

