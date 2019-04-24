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
  
Especifica a versão completa e informações de compilação sobre o servidor do Microsoft Exchange para o qual as contas de um perfil estão conectadas.
  
## 

|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_PROFILE_SERVER_FULL_VERSION  <br/> |
|Identificador:  <br/> |0x663B  <br/> |
|Tipo de propriedade:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Configuração de perfil MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Um perfil pode especificar uma ou mais contas que se conectam a um servidor do Exchange, mas devem estar conectadas ao mesmo servidor Exchange.
  
As versões do Outlook anteriores ao Microsoft Office Outlook 2007 não oferecem suporte a essa propriedade. Para essas versões do Outlook, verifique a existência de **[PR_PROFILE_SERVER_VERSION](pidtagprofileserverversion-canonical-property.md)** no perfil. 
  
Geralmente, se a caixa de correio ativa estiver conectada a um servidor Exchange, o Outlook 2007 armazenará informações completas de versão do Exchange Server na propriedade **PR_PROFILE_SERVER_FULL_VERSION** no perfil ativo. O Outlook armazena as informações em uma estrutura do **EXCHANGE_STORE_VERSION_NUM** que contém os números de versão principal e secundária e os números de compilação principal e secundário. Por exemplo, para armazenar o identificador de versão do Exchange Server do **8.0.685.24**, o número da versão principal é 8 e o número da versão secundária é 0 e o número da compilação principal é 685 e o número de compilação secundário é 24.
  
Somente um de **PR_PROFILE_SERVER_VERSION** ou **PR_PROFILE_SERVER_FULL_VERSION** provavelmente existirá em um perfil, mas não há garantia de que o sempre exista em um perfil. O Outlook não grava em nenhuma propriedade até que tenha se conectado com êxito ao servidor Exchange. 
  
No modelo de objeto do Outlook, você pode usar a propriedade **ExchangeMailboxServerVersion** do objeto **namespace** para localizar a versão do Exchange Server em que a caixa de correio ativa está hospedada. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações do protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece definições de conjunto de propriedades.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs. h
  
> Fornece definições de tipo de dados.
    
Mapitags. h
  
> Contém definições de propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

