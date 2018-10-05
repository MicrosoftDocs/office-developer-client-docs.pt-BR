---
title: Propriedade canônica PidTagAnr
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAnr
api_type:
- HeaderDef
ms.assetid: eca3d4ff-2e92-4d20-a498-98e0773c1962
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: ce08ba971662b7f5060e6b24a6d2c5ee1a921d5b
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400436"
---
# <a name="pidtaganr-canonical-property"></a>Propriedade canônica PidTagAnr

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém um valor de cadeia de caracteres para uso em uma restrição de propriedade em uma tabela de conteúdo de contêiner de catálogo de endereço. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_ANR, PR_ANR_A, PR_ANR_W  <br/> |
|Identificador:  <br/> |0x360C  <br/> |
|Tipo de dados:  <br/> |PT_UNICODE, PT_STRING8  <br/> |
|Área:  <br/> |Catálogo de endereços  <br/> |
   
## <a name="remarks"></a>Comentários

Essas propriedades não pertencem a qualquer objeto; ele é fornecido por provedores de catálogo de endereços nas estruturas de [SPropertyRestriction](spropertyrestriction.md) . Essa propriedade contém uma cadeia de caracteres de (ANR) de resolução de nome ambígua que pode ser testada em relação à tabela de conteúdo de um contêiner catálogo de endereços para localizar os destinatários da mensagem correspondente. 
  
Provedores de catálogo de endereços correspondem ao valor de **PR_ANR** e propriedades associadas em relação a cada entrada na tabela de conteúdo, usando um algoritmo de correspondência definido pelo provedor. A coluna ou colunas que são usadas nessa correspondência são escolhidas pelo provedor como parte do algoritmo. A coluna **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) é o mais usada; a coluna **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) também é útil quando ela contém o nome de email do usuário. 
  
Para obter mais informações sobre a resolução de nome ambígua, consulte [Restrições de catálogo de endereços](address-book-restrictions.md). 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a relacionados especificações de protocolo do Exchange Server.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Especifica as propriedades e operações para obter listas de usuários, contatos, grupos e recursos.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições das propriedades listadas como propriedades associadas.
    
## <a name="see-also"></a>Confira também



[IAddrBook::ResolveName](iaddrbook-resolvename.md)
  
[IABContainer::ResolveNames](iabcontainer-resolvenames.md)


[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

