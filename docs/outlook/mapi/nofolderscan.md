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
  
Especifica se o Microsoft Office Outlook deve examinar pastas de contatos em um repositório.
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Exposto em:  <br/> |[IMsgStore: objeto IMAPIProp](imsgstoreimapiprop.md)  <br/> |
|Criado por:  <br/> |Provedor de repositório  <br/> |
|AcEssado por:  <br/> |Outlook e outros clientes  <br/> |
|Tipo de propriedade:  <br/> |PT_LONG  <br/> |
|Tipo de acesso:  <br/> |Somente leitura ou leitura/gravação dependendo do provedor de repositório  <br/> |
   
## <a name="remarks"></a>Comentários

Para fornecer qualquer uma das funcionalidades de armazenamento, o provedor de repositório deve implementar [IMAPIProp: IUnknown](imapipropiunknown.md) e retornar uma marca de propriedade válida para qualquer uma dessas propriedades passadas para uma chamada [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) . Quando a marca de propriedade para qualquer uma dessas propriedades é passada para [IMAPIProp::](imapiprop-getprops.md)GetProps, o provedor de repositório também deve retornar o valor de propriedade correto. Os provedores de repositório podem chamar o [HrGetOneProp](hrgetoneprop.md) e o [HrSetOneProp](hrsetoneprop.md) para obter ou definir essas propriedades. 
  
Para recuperar o valor dessa propriedade, o cliente deve primeiro usar [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) para obter a marca de propriedade e, em seguida, especificar essa marca de propriedade em [IMAPIProp::](imapiprop-getprops.md) GetProps para obter o valor. Ao chamar [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md), especifique os seguintes valores para a estrutura [MAPINAMEID](mapinameid.md) indicada pelo parâmetro de entrada _lppPropNames_:
  
|||
|:-----|:-----|
|lpGuid:  <br/> |PSETID_Common  <br/> |
|ulKind:  <br/> |MNID_STRING  <br/> |
|Tipo. lpwstrName:  <br/> |L "NoFolderScan"  <br/> |
   
Esta propriedade oferece uma maneira de os provedores de loja especificarem para que o Outlook não examine as pastas de contatos no repositório para evitar a degradação de desempenho. É usado em operações de mala direta durante as quais o Outlook verifica a presença e o valor dessa propriedade antes de iniciar a verificação.
  
Por padrão, essa propriedade não é exposta em um repositório, o que significa que o Outlook pode verificar a pasta de contatos no repositório. Se a propriedade for exposta, estes são os valores possíveis:
  
- Zero (0): o Outlook pode realizar a verificação.
    
- Valor diferente de zero: o Outlook não deve examinar pastas de contatos na loja.
    

