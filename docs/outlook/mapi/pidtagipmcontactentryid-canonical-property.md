---
title: Propriedade canônica PidTagIpmContactEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIpmContactEntryId
api_type:
- HeaderDef
ms.assetid: fccbbb15-dd08-4310-83d7-bf57eb3ed5de
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: a230e13bf81c83504a9da1b0f8d0cd340eb18403
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769382"
---
# <a name="pidtagipmcontactentryid-canonical-property"></a>Propriedade canônica PidTagIpmContactEntryId

  
  
**Aplica-se a**: Outlook 
  
Contém a **EntryID** da pasta Contatos do Outlook. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_IPM_CONTACT_ENTRYID  <br/> |
|Identificador:  <br/> |0x36D1  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Folder  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade é armazenada na pasta caixa de entrada e na pasta raiz do repositório de mensagem. Para acessar a propriedade em um repositório de mensagem específicos, faça o seguinte: 
  
1. Em primeiro lugar, procure a propriedade na pasta caixa de entrada. Use **IMsgStore::GetReceiveFolder** para obter uma referência para a **EntryID** da pasta de caixa de entrada. 
    
2. Se **IMsgStore::GetReceiveFolder** for bem-sucedida, em seguida, use a referência a **EntryID** da caixa de entrada e **IMsgStore::OpenEntry** para abrir a caixa de entrada e obter uma referência a um objeto **IMAPIFolder** . 
    
3. Se **IMsgStore::OpenEntry** for bem-sucedida, em seguida, use a referência retornada ao objeto **IMAPIFolder** e **IMAPIProp::GetProps** para obter a propriedade desejada. 
    
4. Se a etapa 1, 2 ou 3 falhar, procure a propriedade na pasta raiz. Para fazer isso, use **IMsgStore::OpenEntry**, especificando nulo para * * lpEntryID * *, para abrir a pasta raiz do armazenamento de mensagens e obter uma referência ao objeto **IMAPIFolder** . 
    
5. Se abrir a pasta raiz for bem-sucedida, em seguida, use a referência retornada ao objeto **IMAPIFolder** e **IMAPIProp::GetProps** para obter a propriedade desejada. 
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a relacionados especificações de protocolo do Exchange Server.
    
[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)
  
> Especifica as propriedades e operações para a criação e a localização de pastas especiais em uma caixa de correio.
    
[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)
  
> Especifica os métodos para conexão e a configuração de caixas de correio conforme representantes e as interações com objetos de mensagem e o calendário quando eles ajam em nome de outro usuário.
    
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

