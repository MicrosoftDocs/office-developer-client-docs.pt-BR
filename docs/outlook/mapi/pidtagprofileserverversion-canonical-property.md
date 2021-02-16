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
ms.openlocfilehash: 84ff229e9914ec9074d61023873279b110fb606a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286563"
---
# <a name="pidtagprofileserverversion-canonical-property"></a>Propriedade canônica PidTagProfileServerVersion

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Especifica informações sobre a versão do Microsoft Exchange Server à qual as contas em um perfil do Microsoft Outlook estão conectadas.
  
## 

|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_PROFILE_SERVER_VERSION  <br/> |
|Identificador:  <br/> |0x661B  <br/> |
|Tipo de propriedade:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Configuração de perfil MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Um perfil pode especificar uma ou mais contas que se conectam a um Exchange Server, mas devem estar conectadas ao mesmo Exchange Server.
  
Versões do Outlook anteriores ao Microsoft Office Outlook 2007 podem gravar nessa propriedade para armazenar informações sobre a versão do Exchange Server à qual o perfil ativo está conectado. No entanto, o formato das informações de versão varia para diferentes versões do Exchange Server. Por exemplo, o Outlook armazena em **PR_PROFILE_SERVER_VERSION** o valor decimal 6944 para representar apenas o número de com build principal no identificador de versão **6.5.6944.3** do Microsoft Exchange Server 2003. Para uma conexão com o Exchange 2007, o Outlook armazena o número da versão principal e o número de build principal em uma representação hexadecimal concatenada desses números na propriedade. Um identificador de versão do Exchange 2007 de **8.0.685.24** tem um número de versão principal 8 e um número de com build principal 685 em decimal. Convertendo ambos os números em hexadecimais, você 0x8 e 0x2AD. Concatenando esses dois números, o Outlook armazena o valor 0x82AD **em** PR_PROFILE_SERVER_VERSION em representação hexadecimal. 
  
O Outlook 2007 não lê nem escreve nessa propriedade. Ele dá suporte **[PR_PROFILE_SERVER_FULL_VERSION](pidtagprofileserverfullversion-canonical-property.md)**. 
  
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

