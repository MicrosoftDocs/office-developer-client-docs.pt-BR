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
ms.openlocfilehash: 41fdaf333084b7d567f4e67ae9fd2638a1731349
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409661"
---
# <a name="pidtagaddressbookchoosedirectoryautomatically-canonical-property"></a>Propriedade canônica PidTagAddressBookChooseDirectoryAutomatically

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Permite que o Microsoft Outlook 2010 e o Microsoft Outlook 2013 escolham a lista de endereços global (GAL) ou a pasta de contatos mais apropriada para a caixa de correio atual.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY  <br/> |
|Identificador:  <br/> |0x3D1C000B  <br/> |
|Tipo de propriedade:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |Catálogo de endereços  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade corresponde à configuração Escolher **automaticamente** na caixa de diálogo Opções do Address Book. Quando essa propriedade existe na seção de perfil do IID_CAPONE_PROF e está definida como **true**, a caixa de diálogo do Address Book não é mais padrão para o contêiner especificado pelo método [SetDefaultDir,](iaddrbook-setdefaultdir.md) mas escolhe um livro de endereços que o Outlook 2010 ou o Outlook 2013 considera apropriado para o contexto no qual a caixa de diálogo foi exibida. Observe que isso pode resultar em uma experiência ruim para provedores de agendas de terceiros. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Arquivos de header

Mapitags.h
  
> Contém definições de propriedades listadas como propriedades associadas.
    
Mapidefs.h
  
> Fornece definições de tipo de dados.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Constantes MAPI](mapi-constants.md)
  
[Mapeando nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapeando nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

