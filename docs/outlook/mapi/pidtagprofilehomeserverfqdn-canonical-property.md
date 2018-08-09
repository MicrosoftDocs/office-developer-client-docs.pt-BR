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
ms.openlocfilehash: 398ff2fd4bab49c8279e198e3efa416c53abda7c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769681"
---
# <a name="pidtagprofilehomeserverfqdn-canonical-property"></a>Propriedade canônica PidTagProfileHomeServerFQDN

  
  
**Aplica-se a**: Outlook 
  
Habilita a autenticação Kerberos de uma configuração de perfil.
  
****

|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_PROFILE_HOME_SERVER_FQDN  <br/> |
|Identificador:  <br/> |0x662A001F  <br/> |
|Tipo de dados:  <br/> |PT_UNICODE  <br/> |
|Área:  <br/> |Configuração de perfil MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

A definição dessa propriedade para o nome de domínio do servidor de diretório do usuário permite que a conexão direta para a Domain Controller (DC), que é necessário para um perfil que tenha sido configurado para usar a autenticação Kerberos em relação a Microsoft Exchange Server 2007 e nas versões anteriores, definindo **RPC_C_AUTHN_GSS_KERBEROS** em **PR_PROFILE_AUTH_PACKAGE**.
  
> [!NOTE]
> Microsoft Exchange Server 2010 e Exchange Server 2013 lidar com chamadas de catálogo de endereços feitas ao servidor de acesso de cliente forma diferente a partir da maneira em que o Exchange Server 2007 e versões anteriores-los pessoalmente. O processo de DSProxy não é mais usado, portanto a autenticação Kerberos talvez tenham êxito. No entanto, o cliente ainda seria se comunicar com o Exchange server, em vez de diretamente com o controlador de domínio, não pode ser desejável: configuração **PR_PROFILE_HOME_SERVER_FQDN** evita isso. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a relacionados especificações de protocolo do Exchange Server.
    
[[MS-OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)
  
> Especifica as operações permitidas para os objetos do repositório de mensagem principal.
    
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

