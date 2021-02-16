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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357614"
---
# <a name="pidlidcustomflag-canonical-property"></a>Propriedade canônica PidLidCustomFlag

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Uma máscara de bits que especifica como uma mensagem é personalizada, por exemplo, salva com propriedades personalizadas.
  
## 

|||
|:-----|:-----|
|Propriedades associadas:  <br/> |dispidCustomFlag  <br/> |
|Long ID (LID):  <br/> |0x00008251  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
   
## <a name="remarks"></a>Comentários

Para recuperar o valor dessa propriedade, primeiro use **[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)** para obter a marca de propriedade e especifique essa marca de propriedade em **[IMAPIProp::GetProps](imapiprop-getprops.md)** para obter o valor. 
  
Os Sinalizadores possíveis são os seguinte:
  
****

|**Constante**|**Valor**|
|:-----|:-----|
|INSP_ONEOFFFLAGS  <br/> |0x0D000000  <br/> |
|INSP_PROPDEFINITION  <br/> |0x02000000  <br/> |
   
Ao chamar **IMAPIProp::GetIDsFromNames**, especifique os seguintes valores para a **[estrutura MAPINAMEID](mapinameid.md)** apontada pelo parâmetro de entrada  *lppPropNames*  . 
  
****

|**Membro**|**Valor**|
|:-----|:-----|
|lpGuid:  <br/> |PSETID_Common  <br/> |
|ulKind:  <br/> |MNID_ID  <br/> |
|Kind.lID:  <br/> |dispidCustomFlag  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece definições de conjunto de propriedades.
    
### <a name="header-files"></a>Arquivos de header

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições de propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapeando nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapeando nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

