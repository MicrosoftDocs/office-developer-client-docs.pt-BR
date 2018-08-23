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
ms.openlocfilehash: 3416bc50e4628df2be09f9fe1a22d19530bcdff8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578049"
---
# <a name="nofolderscan"></a>NoFolderScan

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Especifica se o Microsoft Office Outlook deve verificar as pastas de contatos em um repositório.
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Expostas no:  <br/> |[IMsgStore: IMAPIProp](imsgstoreimapiprop.md) objeto  <br/> |
|Criados por:  <br/> |Provedor de armazenamento  <br/> |
|Acessado por:  <br/> |Outlook e outros clientes  <br/> |
|Tipo de propriedade:  <br/> |PT_LONG  <br/> |
|Tipo de acesso:  <br/> |Somente leitura ou leitura/gravação, dependendo do provedor de repositório  <br/> |
   
## <a name="remarks"></a>Comentários

Para fornecer qualquer funcionalidade loja, o provedor de repositório deve implementar [IMAPIProp: IUnknown](imapipropiunknown.md) e retornar uma marca de propriedade válido para qualquer uma dessas propriedades passados para uma chamada [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) . Quando a marca de propriedade para qualquer uma dessas propriedades é passada para [IMAPIProp::GetProps](imapiprop-getprops.md), o provedor de armazenamento também deve retornar o valor da propriedade correto. Provedores de armazenamento podem chamar [HrGetOneProp](hrgetoneprop.md) e [HrSetOneProp](hrsetoneprop.md) para obter ou definir essas propriedades. 
  
Para recuperar o valor dessa propriedade, o cliente deve primeiro usar [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) para obter a marca de propriedade e especifique nesta marca de propriedade em [IMAPIProp::GetProps](imapiprop-getprops.md) para obter o valor. Ao chamar [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), especifique os seguintes valores para a estrutura [MAPINAMEID](mapinameid.md) apontado pelo parâmetro de entrada _lppPropNames_:
  
|||
|:-----|:-----|
|lpGuid:  <br/> |PSETID_Common  <br/> |
|ulKind:  <br/> |MNID_STRING  <br/> |
|Kind.lpwstrName:  <br/> |L "NoFolderScan"  <br/> |
   
Essa propriedade oferece uma maneira de provedores de armazenamento especificar como o Outlook não para examinar as pastas de contatos no repositório de para evitar a diminuição do desempenho. Ele é usado nas operações de mala direta durante o qual o Outlook verifica a presença e o valor dessa propriedade antes de iniciar a varredura.
  
Por padrão, essa propriedade não está exposta em um repositório, o que significa que o Outlook pode examinar a pasta de contatos no repositório. Se a propriedade é exposta, estes são os valores possíveis:
  
- Zero (0): Outlook pode executar a verificação.
    
- Valor diferente de zero: o Outlook não deve examinar as pastas de contatos no repositório.
    

