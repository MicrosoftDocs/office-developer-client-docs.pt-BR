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

A definição dessa propriedade com o Nome de Domínio do servidor de diretório do usuário permite a conexão direta com o Controlador de Domínio (DC), que é necessário para um perfil que tenha sido configurado para usar a autenticação Kerberos no Microsoft Exchange Server 2007 e em versões anteriores, definindo o **RPC_C_AUTHN_GSS_KERBEROS** em **PR_PROFILE_AUTH_PACKAGE**.
  
> [!NOTE]
> O Microsoft Exchange Server 2010 e o Exchange Server 2013 lidam com chamadas do livro de endereços feitas ao Servidor de Acesso para Cliente de maneira diferente da maneira como o Exchange Server 2007 e versões anteriores as lidam. O processo DSProxy não é mais usado, portanto, a autenticação Kerberos pode ter êxito. No entanto, o cliente ainda estaria se comunicando com o servidor Exchange em  vez de diretamente com o DC, o que pode não ser desejado: a configuração PR_PROFILE_HOME_SERVER_FQDN evita isso. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a especificações de protocolo relacionadas do Exchange Server.
    
[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)
  
> Especifica operações permitidas para os objetos principais do armazenamento de mensagens.
    
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

