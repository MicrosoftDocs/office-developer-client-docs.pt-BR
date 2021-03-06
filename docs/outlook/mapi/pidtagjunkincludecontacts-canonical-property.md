---
title: Propriedade canônica PidTagJunkIncludeContacts
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagJunkIncludeContacts
api_type:
- HeaderDef
ms.assetid: 25368f6c-4fba-4381-840c-ca122bd31b5f
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7e61e98d1db1ab3acb958da353d8d22870937632
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328711"
---
# <a name="pidtagjunkincludecontacts-canonical-property"></a>Propriedade canônica PidTagJunkIncludeContacts

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Indica se os endereços de email dos contatos na pasta Contatos são tratados especialmente em relação ao filtro de spam.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_JUNK_INCLUDE_CONTACTS  <br/> |
|Identificador:  <br/> |0x6100  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Spam  <br/> |
   
## <a name="remarks"></a>Comentários

Se definido como "0x00000001", esses endereços de email deverão preencher a parte do endereço de email de contato "confiável" da Restrição de Regra de Lixo Eletrônico de forma que os emails desses endereços seja tratados como "não é lixo eletrônico". Se definido como "0x00000000", os endereços de email da pasta Contatos não devem ser adicionados à Regra de Lixo Eletrônico e a seção da regra deve ser NULL.
  
Se essa propriedade estiver presente com um valor de "0x00000001" e se o contato adicionado tiver endereços de email que ainda não estão incluídos na seção contatos confiáveis da Regra de Lixo Eletrônico, esses endereços de email deverão ser adicionados à restrição. Se essa propriedade for "0x00000000", nenhuma ação será necessária.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a especificações de protocolo relacionadas do Exchange Server.
    
[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> Permite a manipulação de listas de bloqueio/autorização e a determinação de mensagens de lixo eletrônico.
    
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

