---
title: NoFolderScan
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4949aef9-4c96-82cc-cd13-57981e07cc40
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: fc5f5a42e2b1e57374ff80a9333b927cc8dba120
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436797"
---
# <a name="nofolderscan"></a>NoFolderScan

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Especifica se o Microsoft Office Outlook deve verificar pastas de Contatos em um armazenamento.
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Exposto em:  <br/> |[IMsgStore : objeto IMAPIProp](imsgstoreimapiprop.md)  <br/> |
|Criado por:  <br/> |Provedor da Loja  <br/> |
|Acessado por:  <br/> |Outlook e outros clientes  <br/> |
|Tipo de propriedade:  <br/> |PT_LONG  <br/> |
|Tipo de acesso:  <br/> |Somente leitura ou leitura/gravação, dependendo do provedor da loja  <br/> |
   
## <a name="remarks"></a>Comentários

Para fornecer qualquer uma das funcionalidades do armazenamento, o provedor de armazenamento deve implementar [IMAPIProp : IUnknown](imapipropiunknown.md) e retornar uma marca de propriedade válida para qualquer uma dessas propriedades passadas para uma chamada [IMAPIProp::GetIDsFromNames.](imapiprop-getidsfromnames.md) Quando a marca de propriedade de qualquer uma dessas propriedades é passada para [IMAPIProp::GetProps](imapiprop-getprops.md), o provedor de armazenamento também deve retornar o valor de propriedade correto. Os provedores da loja podem [chamar HrGetOneProp](hrgetoneprop.md) e [HrSetOneProp](hrsetoneprop.md) para obter ou definir essas propriedades. 
  
Para recuperar o valor dessa propriedade, o cliente deve primeiro usar [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) para obter a marca de propriedade e, em seguida, especificar essa marca de propriedade em [IMAPIProp::GetProps](imapiprop-getprops.md) para obter o valor. Ao chamar [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), especifique os seguintes valores para a [estrutura MAPINAMEID](mapinameid.md) apontada pelo parâmetro de entrada  _lppPropNames_:
  
|||
|:-----|:-----|
|lpGuid:  <br/> |PSETID_Common  <br/> |
|ulKind:  <br/> |MNID_STRING  <br/> |
|Kind.lpwstrName:  <br/> |L"NoFolderScan"  <br/> |
   
Essa propriedade fornece uma maneira para os provedores de armazenamento especificarem para o Outlook não verificar pastas de contatos no armazenamento para evitar a degradação do desempenho. Ele é usado em operações de mala direta durante as quais o Outlook verifica a presença e o valor dessa propriedade antes de iniciar a verificação.
  
Por padrão, essa propriedade não é exposta em um armazenamento, o que significa que o Outlook pode verificar a pasta Contatos no armazenamento. Se a propriedade for exposta, os valores possíveis serão os seguintes:
  
- Zero (0): o Outlook pode realizar a verificação.
    
- Valor diferente de zero: o Outlook não deve verificar pastas de contatos no armazenamento.
    

