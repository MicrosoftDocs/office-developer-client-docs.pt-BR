---
title: Propriedade canônica PidTagProfileServerVersion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5d41a536-81ff-733c-2fd7-460798e057c8
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 571ac25d6bc738f8289e3019c342820682d08c28
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769685"
---
# <a name="pidtagprofileserverversion-canonical-property"></a>Propriedade canônica PidTagProfileServerVersion

  
  
**Aplica-se a**: Outlook 
  
Especifica informações sobre a versão do Microsoft Exchange Server ao qual contas em um perfil do Microsoft Outlook estão conectadas.
  
## 

|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_PROFILE_SERVER_VERSION  <br/> |
|Identificador:  <br/> |0x661B  <br/> |
|Tipo de propriedade:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Configuração de perfil MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Um perfil pode especificar uma ou mais contas que se conectam ao servidor do Exchange, mas eles devem estar conectados ao mesmo servidor Exchange.
  
Versões do Outlook anteriores ao Microsoft Office Outlook 2007 podem gravar essa propriedade para armazenar informações sobre a versão do Exchange Server ao qual o perfil ativo está conectado. No entanto, o formato das informações de versão varia para versões diferentes do Exchange Server. Por exemplo, repositórios do Outlook no **PR_PROFILE_SERVER_VERSION** o valor decimal 6944 para representar somente as principais número do identificador de versão de compilação **6.5.6944.3** para Microsoft Exchange Server 2003. Para uma conexão do Exchange 2007, Outlook armazena o número de versão principal e número em uma representação hexadecimal concatenada desses números na propriedade da compilação do principal. Um identificador de versão do Exchange 2007 de **8.0.685.24** tem um número de versão principal 8 e um número de compilação principais 685 em decimal. Conversão de ambos os números em hexadecimal, você obtém 0x8 e 0x2AD. Concatenando esses dois números, o Outlook armazena o valor 0x82AD em **PR_PROFILE_SERVER_VERSION** na representação hexadecimal. 
  
O Outlook 2007 não ler ou gravar a essa propriedade. Suporte a **[PR_PROFILE_SERVER_FULL_VERSION](pidtagprofileserverfullversion-canonical-property.md)**. 
  
Somente uma das **PR_PROFILE_SERVER_VERSION** ou **PR_PROFILE_SERVER_FULL_VERSION** é provável que existam em um perfil, mas há nenhuma garantia de que um sempre existe em um perfil. Outlook não gravar ou propriedade até que tenha se conectado com êxito ao servidor do Exchange. 
  
No modelo de objeto do Outlook, você pode usar a propriedade **ExchangeMailboxServerVersion** do objeto **NameSpace** para localizar a versão do Exchange Server no qual a caixa de correio ativa está hospedada. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
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

