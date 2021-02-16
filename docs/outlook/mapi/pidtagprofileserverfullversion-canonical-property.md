---
title: Propriedade canônica PidTagProfileServerFullVersion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8c88a625-da57-3b1d-9887-0a898b722766
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 9456178e9426d7a5fe17382d876f507daa0251f4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341598"
---
# <a name="pidtagprofileserverfullversion-canonical-property"></a>Propriedade canônica PidTagProfileServerFullVersion

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Especifica informações completas de versão e build sobre o Microsoft Exchange Server às quais as contas em um perfil estão conectadas.
  
## 

|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_PROFILE_SERVER_FULL_VERSION  <br/> |
|Identificador:  <br/> |0x663B  <br/> |
|Tipo de propriedade:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Configuração de perfil MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Um perfil pode especificar uma ou mais contas que se conectam a um Exchange Server, mas devem estar conectadas ao mesmo Exchange Server.
  
As versões do Outlook anteriores ao Microsoft Office Outlook 2007 não são suportadas por essa propriedade. Para essas versões do Outlook, verifique a existência **[de PR_PROFILE_SERVER_VERSION](pidtagprofileserverversion-canonical-property.md)** no perfil. 
  
Geralmente, se **a** caixa de correio ativa estiver conectada a um Exchange Server, o Outlook 2007 armazenará informações completas da versão do Exchange Server na PR_PROFILE_SERVER_FULL_VERSION no perfil ativo. Outlook stores the information in an **EXCHANGE_STORE_VERSION_NUM** structure that contains the major and minor version numbers and the major and minor build numbers. Por exemplo, para armazenar o identificador de versão do Exchange Server de **8.0.685.24**, o número da versão principal é 8 e o número da versão secundária é 0, e o número de com build principal é 685 e o número de com build secundário é 24.
  
Apenas um dos **PR_PROFILE_SERVER_VERSION** **ou PR_PROFILE_SERVER_FULL_VERSION** provavelmente existirá em um perfil, mas não há garantia de que sempre exista em um perfil. O Outlook não gravará em nenhuma das propriedades até que tenha se conectado com êxito ao Exchange Server. 
  
No modelo de objeto do Outlook, você pode usar a propriedade **ExchangeMailboxServerVersion** do objeto **NameSpace** para encontrar a versão do Exchange Server na qual a caixa de correio ativa está hospedada. 
  
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

