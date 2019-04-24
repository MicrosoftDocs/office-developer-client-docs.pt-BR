---
title: Propriedade canônica PidTagProfileHomeServerFQDN
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 80273b50-bc16-4be2-8471-1a127b6786bb
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: aef4a932da35f3c4955bc2f4b265b146775c6d87
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341591"
---
# <a name="pidtagprofilehomeserverfqdn-canonical-property"></a>Propriedade canônica PidTagProfileHomeServerFQDN

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Habilita a autenticação Kerberos de uma configuração de perfil.
  
****

|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_PROFILE_HOME_SERVER_FQDN  <br/> |
|Identificador:  <br/> |0x662A001F  <br/> |
|Tipo de dados:  <br/> |PT_UNICODE  <br/> |
|Área:  <br/> |Configuração de perfil MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

A definição dessa propriedade como o nome de domínio do servidor de diretório do usuário permite a conexão direta com o controlador de domínio (DC), que é necessário para um perfil configurado para usar a autenticação Kerberos no Microsoft Exchange Server 2007 e versões anteriores, definindo **RPC_C_AUTHN_GSS_KERBEROS** em **PR_PROFILE_AUTH_PACKAGE**.
  
> [!NOTE]
> O Microsoft Exchange Server 2010 e o Exchange Server 2013 lidam com chamadas de catálogo de endereços feitas ao servidor de acesso para cliente de forma diferente da forma como o Exchange Server 2007 e versões anteriores as manipulam. O processo DSProxy não é mais usado, portanto a autenticação Kerberos pode ter êxito. No enTanto, o cliente ainda estaria se comunicando com o servidor do Exchange, em vez de diretamente com o DC, o que pode não ser desejado: a configuração do **PR_PROFILE_HOME_SERVER_FQDN** evita isso. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações do protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências às especificações relacionadas do protocolo do Exchange Server.
    
[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)
  
> Especifica operações permitidas para os principais objetos do repositório de mensagens.
    
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

