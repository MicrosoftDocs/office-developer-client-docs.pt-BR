---
title: Propriedade canônica PidTagAddressBookChooseDirectoryAutomatically
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cecd0679-4bc2-4399-8f89-a4e17bb909a0
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 48dfced07a8fd78a1af22679759effbd3c6da343
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768925"
---
# <a name="pidtagaddressbookchoosedirectoryautomatically-canonical-property"></a>Propriedade canônica PidTagAddressBookChooseDirectoryAutomatically

  
  
**Aplica-se a**: Outlook 
  
Permite que o Microsoft Outlook 2010 e o Microsoft Outlook 2013 escolher a lista de endereços global (GAL) mais apropriada ou pasta de contatos para a caixa de correio atual.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY  <br/> |
|Identificador:  <br/> |0x3D1C000B  <br/> |
|Tipo de propriedade:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |Catálogo de endereços  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade corresponde à configuração da **Escolha automaticamente** na caixa de diálogo Opções do catálogo de endereços. Quando essa propriedade existe na seção de perfil IID_CAPONE_PROF e estiver definida como **true**, o catálogo de endereços diálogo não mais padrões para o contêiner especificado pelo método [SetDefaultDir](iaddrbook-setdefaultdir.md) , mas escolhe um catálogo de endereços que o Outlook 2010 ou Outlook 2013 considera apropriada para o contexto no qual a caixa de diálogo foi exibida. Observe que isso pode resultar em uma experiência ruim para provedores de catálogo de endereços de terceiros. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Arquivos de cabeçalho

Mapitags.h
  
> Contém definições das propriedades listadas como propriedades associadas.
    
Mapidefs.h
  
> Fornece definições de tipo de dados.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Constantes MAPI](mapi-constants.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

