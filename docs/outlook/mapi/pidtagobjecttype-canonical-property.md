---
title: Propriedade canônica PidTagObjectType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagObjectType
api_type:
- HeaderDef
ms.assetid: 37da4ff5-300d-479f-a8b4-6fc36df997d9
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: b433db7cb157afbf8c3b506f2ed95b04b7b88564
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329222"
---
# <a name="pidtagobjecttype-canonical-property"></a>Propriedade canônica PidTagObjectType

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém o tipo de um objeto. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_OBJECT_TYPE  <br/> |
|Identificador:  <br/> |0x0FFE  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Comum  <br/> |
   
## <a name="remarks"></a>Comentários

O tipo de objeto contido nessa propriedade corresponde à interface principal disponível para um objeto acessível por meio da interface **OpenEntry.** Geralmente, ele é obtido consultando o parâmetro  _lpulObjType_ retornado pelo **método OpenEntry** apropriado. Quando a interface for obtida de outras maneiras, chame [IMAPIProp::GetProps](imapiprop-getprops.md) para obter o valor dessa propriedade. 
  
Essa propriedade pode ter exatamente um dos seguintes valores:
  
MAPI_ABCONT 
  
> Objeto de contêiner do livro de endereços 
    
MAPI_ADDRBOOK 
  
> Objeto address book 
    
MAPI_ATTACH 
  
> Objeto message attachment 
    
MAPI_DISTLIST 
  
> Objeto de lista de distribuição 
    
MAPI_FOLDER 
  
> Objeto Folder 
    
MAPI_FORMINFO 
  
> Objeto Form 
    
MAPI_MAILUSER 
  
> Objeto de usuário de mensagens 
    
MAPI_MESSAGE 
  
> Objeto Message 
    
MAPI_PROFSECT 
  
> Objeto da seção Profile 
    
MAPI_SESSION 
  
> Objeto Session 
    
MAPI_STATUS 
  
> Objeto Status 
    
MAPI_STORE 
  
> Objeto de armazenamento de mensagens
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a especificações de protocolo relacionadas do Exchange Server.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Especifica as propriedades e operações para listas de usuários, contatos, grupos e recursos.
    
[[MS-NSPI]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)
  
> Lida com as comunicações de um cliente com um servidor NSPI (Name Service Provider Interface).
    
[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> Lida com operações de pasta.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Lida com a ordem e o fluxo para transferências de dados entre um cliente e um servidor.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Converte de convenções de email padrão da Internet em objetos de mensagem.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Lida com objetos de mensagem e anexo.
    
[[MS-OXOAB]](https://msdn.microsoft.com/library/b4750386-66ec-4e69-abb6-208dd131c7de%28Office.15%29.aspx)
  
> Especifica os formatos de arquivo do OAB (address book) offline para o cache de objetos do livro de endereços local.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica as propriedades e operações que são permitidas para objetos de mensagem de email.
    
[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)
  
> Especifica as propriedades e operações para manipular uma configuração de lista de pastas de pesquisa.
    
### <a name="header-files"></a>Arquivos de header

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições de propriedades listadas como propriedades associadas.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapeando nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapeando nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

