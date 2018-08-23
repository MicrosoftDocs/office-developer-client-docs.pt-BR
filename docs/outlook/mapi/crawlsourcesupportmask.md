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
ms.openlocfilehash: cc8ff946081fb7817f0f6018acefbe31293a13a0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581773"
---
# <a name="crawlsourcesupportmask"></a>CrawlSourceSupportMask

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Especifica se o Microsoft Office Outlook deve verificar pastas em um repositório, incluindo pastas de contatos, calendário e tarefas, na inicialização para preencher o painel de navegação.
  
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
|Kind.lpwstrName:  <br/> |L "CrawlSourceSupportMask"  <br/> |
   
Essa propriedade oferece uma maneira de provedores de armazenamento especificar se o Outlook deve examinar várias pastas em um repositório. Ele é usado na inicialização quando o Outlook verifica as pastas existentes em cada repositório aberto para preencher o painel de **navegação** ; Outlook verifica a presença e o valor dessa propriedade em um repositório antes de iniciar a varredura. 
  
Por padrão, essa propriedade não está exposta em um repositório, o que significa que o Outlook pode examinar pastas no repositório. Se a propriedade é exposta, estes são os valores possíveis:
  
```
enum { 
 CSM_DEFAULT              = 0, 
 CSM_DO_NOT_CRAWL         = 1 << 0x0, 
 CSM_CLIENT_DO_NOT_CHANGE = 1 << 0xF 
};
```

CSM_DEFAULT
  
- O Outlook pode examinar pastas no repositório.
    
CSM_DO_NOT_CRAWL
  
- O Outlook não deve examinar as pastas no repositório.
    
CSM_CLIENT_DO_NOT_CHANGE
  
- Não permitir que os clientes alterar essa propriedade no repositório. Observe que a constante **CSM_CLIENT_DO_NOT_CHANGE** é para referência futura e não está implementado no momento. No momento, um repositório pode impedir que os clientes alterem esse sinalizador por codificar o valor que o repositório retorna para essa propriedade. 
    

