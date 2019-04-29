---
title: CrawlSourceSupportMask
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CrawlSourceSupportMask
api_type:
- COM
ms.assetid: d0a2f7ea-df6a-89e8-18c2-ac92e0a20edc
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: cc3fcedb73b4acbd85529615d857403b4c268f3d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420910"
---
# <a name="crawlsourcesupportmask"></a>CrawlSourceSupportMask

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Especifica se o Microsoft Office Outlook deve verificar pastas em um repositório, incluindo as pastas contatos, calendário e tarefas, na inicialização para preencher o painel de navegação.
  
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
|Tipo. lpwstrName:  <br/> |L "CrawlSourceSupportMask"  <br/> |
   
Essa propriedade oferece uma maneira de os provedores de repositório especificarem se o Outlook deve examinar várias pastas em um repositório. Ele é usado na inicialização quando o Outlook verifica pastas existentes em cada repositório aberto para preencher o painel de **navegação** ; O Outlook verifica a presença e o valor dessa propriedade em um repositório antes de iniciar a verificação. 
  
Por padrão, essa propriedade não é exposta em um repositório, o que significa que o Outlook pode examinar pastas na loja. Se a propriedade for exposta, estes são os valores possíveis:
  
```
enum { 
 CSM_DEFAULT              = 0, 
 CSM_DO_NOT_CRAWL         = 1 << 0x0, 
 CSM_CLIENT_DO_NOT_CHANGE = 1 << 0xF 
};
```

CSM_DEFAULT
  
- O Outlook pode examinar pastas na loja.
    
CSM_DO_NOT_CRAWL
  
- O Outlook não deve verificar pastas na loja.
    
CSM_CLIENT_DO_NOT_CHANGE
  
- Não permita que os clientes alterem essa propriedade na loja. Observe que a constante **CSM_CLIENT_DO_NOT_CHANGE** é para referência futura e não está implementada no momento. Por enquanto, um repositório pode impedir que os clientes alterem esse sinalizador codificando o valor que o repositório retorna para esta propriedade. 
    

