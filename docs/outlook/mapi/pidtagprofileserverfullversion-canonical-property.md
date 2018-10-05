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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396173"
---
# <a name="pidtagprofileserverfullversion-canonical-property"></a>Propriedade canônica PidTagProfileServerFullVersion

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Especifica as informações de versão e compilação completas sobre o Microsoft Exchange Server ao qual contas em um perfil estão conectadas.
  
## 

|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_PROFILE_SERVER_FULL_VERSION  <br/> |
|Identificador:  <br/> |0x663B  <br/> |
|Tipo de propriedade:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Configuração de perfil MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Um perfil pode especificar uma ou mais contas que se conectam ao servidor do Exchange, mas eles devem estar conectados ao mesmo servidor Exchange.
  
Versões do Outlook anteriores ao Microsoft Office Outlook 2007 não têm suporte para essa propriedade. Para as versões do Outlook, verifique a existência de **[PR_PROFILE_SERVER_VERSION](pidtagprofileserverversion-canonical-property.md)** no perfil. 
  
Geralmente, se a caixa de correio ativa estiver conectada a um servidor Exchange, o Outlook 2007 armazena informações de versão completas do Exchange Server na propriedade **PR_PROFILE_SERVER_FULL_VERSION** no perfil ativo. Outlook armazena as informações em uma estrutura **EXCHANGE_STORE_VERSION_NUM** que contém os números da versão principal e secundária e os números de compilação principais e secundárias. Por exemplo, para armazenar o identificador de versão do Exchange Server do **8.0.685.24**, o número de versão principal é 8 e número da versão secundária é 0 e o número de compilação principais é 685 e número da versão secundária está 24.
  
Somente uma das **PR_PROFILE_SERVER_VERSION** ou **PR_PROFILE_SERVER_FULL_VERSION** é provável que existam em um perfil, mas há nenhuma garantia de que um sempre existe em um perfil. Outlook não gravar ou propriedade até que tenha se conectado com êxito ao servidor do Exchange. 
  
No modelo de objeto do Outlook, você pode usar a propriedade **ExchangeMailboxServerVersion** do objeto **NameSpace** para localizar a versão do Exchange Server no qual a caixa de correio ativa está hospedada. 
  
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

