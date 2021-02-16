---
title: Exibir informações do destinatário
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7ffec274-ee90-44c7-ab2e-7dfb502517a6
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: e1c31e5edf702dd8f172f67e7055a96ae4cfff1c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412951"
---
# <a name="displaying-recipient-information"></a>Exibir informações do destinatário

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
MAPI provides a common dialog box for showing recipient details. A caixa de diálogo de detalhes é criada a partir de uma tabela de exibição e de uma **implementação IMAPIProp.** A tabela de exibição descreve a aparência da exibição de detalhes e a implementação **IMAPIProp** controla os dados do destinatário. Seu provedor é responsável por fornecer a tabela de exibição e a **implementação IMAPIProp** para cada destinatário. 
  
A maneira mais fácil de criar a tabela de exibição é definir uma [estrutura DTPAGE](dtpage.md) e chamar [BuildDisplayTable](builddisplaytable.md). No entanto, alguns provedores, especificamente somente leitura que permitem a criação de destinatários únicos, usam **IPropData**. A **implementação IMAPIProp** pode ser qualquer tipo de objeto de propriedade. 
  
Há dois métodos para invocar essa caixa de diálogo: [IAddrBook::D etails](iaddrbook-details.md) e [IMAPISupport::D etails](imapisupport-details.md). Quando seu provedor chama um desses métodos para solicitar detalhes de um destinatário, o MAPI primeiro abre o destinatário chamando o método [IMAPIContainer::OpenEntry](imapicontainer-openentry.md) do contêiner. Em seguida, ele chama o método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) do destinatário para solicitar a **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)). **PR_DETAILS_TABLE** é a propriedade que representa a tabela de exibição de detalhes de um destinatário. 
  
A interface [IPropData : IMAPIProp](ipropdataimapiprop.md) pode ser usada para monitorar alterações nos controles de tabela de exibição, conforme descrito no procedimento a seguir. 
  
## <a name="monitor-changes-to-a-control"></a>Monitorar alterações em um controle
  
1. Antes que o usuário tenha acesso ao controle, chame [IPropData::HrSetObjAccess](ipropdata-hrsetobjaccess.md) para definir o acesso do controle a IPROP_CLEAN. 
    
2. Permitir que o usuário trabalhe com a caixa de diálogo. 
    
3. Quando o usuário tiver terminado, chame [IPropData::HrGetPropAccess](ipropdata-hrgetpropaccess.md) para recuperar o nível de acesso atual do controle. 
    
4. Se o nível de acesso IPROP_DIRTY, o usuário modificou o controle. Seu provedor deve:
    
   - Chame [IPropData::HrSetPropAccess](ipropdata-hrsetpropaccess.md) para definir o nível de acesso de volta para IPROP_CLEAN. 
    
   - Chame o método [IMAPIProp::GetProps](imapiprop-getprops.md) do objeto de dados de propriedade para recuperar a propriedade alterada e atualizá-la chamando [IMAPIProp::SetProps](imapiprop-setprops.md).
    
5. Se o nível de acesso ainda IPROP_CLEAN, o controle não foi modificado. 
    
Para obter mais informações sobre como criar tabelas de exibição, consulte [Display Tables](display-tables.md).
  

