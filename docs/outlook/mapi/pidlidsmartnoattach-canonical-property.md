---
title: Propriedade canônica PidLidSmartNoAttach
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSmartNoAttach
api_type:
- COM
ms.assetid: 60299c1b-1b46-4c3a-8fb9-a2b4d3383aac
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7dddca6a17b07047d1447a57347fbe47a04471e0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331315"
---
# <a name="pidlidsmartnoattach-canonical-property"></a>Propriedade canônica PidLidSmartNoAttach

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Representa se os anexos em uma mensagem são considerados ocultos.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |dispidSmartNoAttach  <br/> |
|Conjunto de propriedades:  <br/> |PSETID_Common  <br/> |
|Long ID (LID):  <br/> |0x00008514  <br/> |
|Tipo de dados:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |Configuração em tempo de execução  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade será TRUE se os anexos da mensagem são considerados ocultos.
  
Ele indica se o objeto de mensagem não tem anexos visíveis do usuário final. Essa propriedade pode estar desa416; em caso afirmativo, será assumido um valor padrão falso.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece definição de conjunto de propriedades e referências a especificações de protocolo relacionadas do Exchange Server.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Lida com objetos de mensagem e anexo.
    
### <a name="header-files"></a>Arquivos de header

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapeando nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapeando nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

