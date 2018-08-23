---
title: IMAPIProp IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp
api_type:
- COM
ms.assetid: 3c9e4e05-cd3a-4b56-9dff-879e33ff6fd5
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: a397ac9110429911755552298ffe244343d54a8a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583726"
---
# <a name="imapiprop--iunknown"></a>IMAPIProp : IUnknown

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Permite que os clientes, provedores de serviços e MAPI trabalhar com propriedades. Todos os objetos que oferecem suporte a propriedades implementam esta interface.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
|Expostos pelo:  <br/> |Nenhum objeto expõe essa interface diretamente.  <br/> |
|Implementada por:  <br/> |Provedores de serviços e MAPI  <br/> |
|Chamado pelo:  <br/> |MAPI, provedores de serviços e aplicativos cliente  <br/> |
|Identificador de interface:  <br/> |IID_IMAPIProp  <br/> |
|Tipo de ponteiro:  <br/> |LPMAPIPROP  <br/> |
|Modelo de transação:  <br/> |Classe abstrata, nunca implementada  <br/> |
   
## <a name="vtable-order"></a>Ordem vtable

|||
|:-----|:-----|
|[GetLastError](imapiprop-getlasterror.md) <br/> |Retorna uma estrutura [MAPIERROR](mapierror.md) que contém informações sobre o erro anterior.  <br/> |
|[SaveChanges](imapiprop-savechanges.md) <br/> |Torna permanente quaisquer alterações feitas a um objeto desde a última operação de salvamento.  <br/> |
|[GetProps](imapiprop-getprops.md) <br/> |Recupera o valor da propriedade de uma ou mais propriedades de um objeto.  <br/> |
|[GetPropList](imapiprop-getproplist.md) <br/> |Retorna as marcas de propriedade para todas as propriedades.  <br/> |
|[OpenProperty](imapiprop-openproperty.md) <br/> |Retorna um ponteiro para uma interface que pode ser usada para acessar uma propriedade.  <br/> |
|[SetProps](imapiprop-setprops.md) <br/> |Atualiza uma ou mais propriedades.  <br/> |
|[DeleteProps](imapiprop-deleteprops.md) <br/> |Exclui uma ou mais propriedades de um objeto.  <br/> |
|[CopyTo](imapiprop-copyto.md) <br/> |Copia ou move todas as propriedades, exceto especificamente propriedades excluídas.  <br/> |
|[CopyProps](imapiprop-copyprops.md) <br/> |Cópias ou movimentações de propriedades selecionadas.  <br/> |
|[GetNamesFromIDs](imapiprop-getnamesfromids.md) <br/> |Fornece os nomes de propriedades que correspondem a um ou mais identificadores de propriedade.  <br/> |
|[GetIDsFromNames](imapiprop-getidsfromnames.md) <br/> |Fornece os identificadores de propriedade que correspondem a um ou mais nomes de propriedade.  <br/> |
   
## <a name="remarks"></a>Comentários

 **IMAPIProp** é a interface de base para as seguintes interfaces: 
  
- [IAttach](iattachimapiprop.md)
    
- [IMailUser](imailuserimapiprop.md)
    
- [IMAPIContainer](imapicontainerimapiprop.md)
    
- [IMAPIFormInfo](imapiforminfoimapiprop.md)
    
- [IMAPIStatus](imapistatusimapiprop.md)
    
- [IMessage](imessageimapiprop.md)
    
- [IMsgStore](imsgstoreimapiprop.md)
    
- [IProfSect](iprofsectimapiprop.md)
    
- [IPropData](ipropdataimapiprop.md)
    
## <a name="see-also"></a>Confira também



[Interfaces MAPI](mapi-interfaces.md)

