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
ms.openlocfilehash: 8f0c79fa098b8bca0518921a25d88a229e23e955
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327899"
---
# <a name="pidtagipmcontactentryid-canonical-property"></a>Propriedade canônica PidTagIpmContactEntryId

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém a **EntryID** da pasta contatos do Outlook. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_IPM_CONTACT_ENTRYID  <br/> |
|Identificador:  <br/> |0x36D1  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Pasta  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade é armazenada na pasta caixa de entrada e na pasta raiz do repositório de mensagens. Para acessar a propriedade em um repositório de mensagens específico, faça o seguinte: 
  
1. Primeiro, procure a propriedade na pasta caixa de entrada. Use **IMsgStore:: GetReceiveFolder** para obter uma referência para a **EntryID** da pasta caixa de entrada. 
    
2. Se **IMsgStore:: GetReceiveFolder** for bem-sucedido, use a referência para a **EntryID** da caixa de entrada e **IMsgStore:: OpenEntry** para abrir a caixa de entrada e obter uma referência a um objeto **IMAPIFolder** . 
    
3. Se **IMsgStore:: OpenEntry** for bem-sucedido, use a referência retornada para o objeto **IMAPIFolder** e **IMAPIProp::** GetProps para obter a propriedade desejada. 
    
4. Se a etapa 1, 2 ou 3 falhar, procure a propriedade na pasta raiz. Para fazer isso, use **IMsgStore:: OpenEntry**, especificando NULL para * * lpEntryID * *, para abrir a pasta raiz do repositório de mensagens e obter uma referência para o objeto **IMAPIFolder** . 
    
5. Se a abertura da pasta raiz for bem-sucedida, use a referência retornada ao objeto **IMAPIFolder** e **IMAPIProp::** GetProps para obter a propriedade desejada. 
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações do protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências às especificações relacionadas do protocolo do Exchange Server.
    
[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)
  
> Especifica as propriedades e operações para criar e localizar as pastas especiais em uma caixa de correio.
    
[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)
  
> Especifica métodos para conectar e configurar caixas de correio como delegados e interações com objetos de mensagem e calendário quando eles atuam em nome de outro usuário.
    
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

