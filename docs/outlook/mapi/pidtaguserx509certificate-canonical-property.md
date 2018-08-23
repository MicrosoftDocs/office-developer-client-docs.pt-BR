---
title: Propriedade canônica PidTagUserX509Certificate
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagUserX509Certificate
api_type:
- COM
ms.assetid: 278bb9e4-3ff6-4bef-b208-7924f7a5e9b1
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7686f36ca105ab92161757d492a86b4b78461dfd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564077"
---
# <a name="pidtaguserx509certificate-canonical-property"></a>Propriedade canônica PidTagUserX509Certificate

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém os certificados de segurança x. 509 versão 3 para um usuário de mensagens. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_USER_X509_CERTIFICATE  <br/> |
|Identificador:  <br/> |0x3A70  <br/> |
|Tipo de dados:  <br/> |PT_MV_BINARY  <br/> |
|Área:  <br/> |Usuário de email MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade é usada pelos aplicativos que utilizam a segurança de chave pública. Ele contém uma representação binária de um ou mais certificados de segurança 3 de versão de x. 509. 
  
Vários aplicativos e clientes podem usar essa propriedade para seus próprios certificados de segurança. O formato binário dos dados x. 509 pode variar entre os fornecedores. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a relacionados especificações de protocolo do Exchange Server.
    
[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Especifica as propriedades e operações para obter listas de usuários, contatos, grupos e recursos.
    
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

