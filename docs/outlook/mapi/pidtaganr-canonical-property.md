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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327962"
---
# <a name="pidtaganr-canonical-property"></a>Propriedade canônica PidTagAnr

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém um valor de cadeia de caracteres para uso em uma restrição de propriedade em uma tabela de conteúdo de contêiner de catálogo de endereços. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_ANR, PR_ANR_A, PR_ANR_W  <br/> |
|Identificador:  <br/> |0x360C  <br/> |
|Tipo de dados:  <br/> |PT_UNICODE, PT_STRING8  <br/> |
|Área:  <br/> |Catálogo de endereços  <br/> |
   
## <a name="remarks"></a>Comentários

Essas propriedades não pertencem a nenhum objeto; Ele é fornecido por provedores de catálogo de endereços nas estruturas do [SPropertyRestriction](spropertyrestriction.md) . Essa propriedade contém uma cadeia de caracteres ANR (resolução de nomes ambíguos) que pode ser testada em uma tabela de conteúdo do contêiner de catálogo de endereços para localizar destinatários de mensagem correspondentes. 
  
Os provedores de catálogos de endereços correspondem ao valor de **PR_ANR** e as propriedades associadas a cada entrada na tabela de conteúdo, usando um algoritmo de correspondência definido pelo provedor. A coluna ou colunas que são usadas nessa correspondência são escolhidas pelo provedor como parte do algoritmo. A coluna **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) é a mais comumente usada; a coluna **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) também é útil quando contém o nome de email do usuário. 
  
Para obter mais informações sobre resolução de nomes ambíguos, consulte [restrições do catálogo de endereços](address-book-restrictions.md). 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações do protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências às especificações relacionadas do protocolo do Exchange Server.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Especifica as propriedades e operações de listas de usuários, contatos, grupos e recursos.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs. h
  
> Fornece definições de tipo de dados.
    
Mapitags. h
  
> Contém definições de propriedades listadas como propriedades associadas.
    
## <a name="see-also"></a>Confira também



[IAddrBook::ResolveName](iaddrbook-resolvename.md)
  
[IABContainer::ResolveNames](iabcontainer-resolvenames.md)


[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

