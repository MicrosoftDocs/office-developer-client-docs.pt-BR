---
title: Exibindo informações do destinatário
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7ffec274-ee90-44c7-ab2e-7dfb502517a6
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 4610d9e643541e39144f2af86a2d64928b8e9ca7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591286"
---
# <a name="displaying-recipient-information"></a>Exibindo informações do destinatário

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
MAPI fornece uma caixa de diálogo comuns para mostrar detalhes do destinatário. A caixa de diálogo detalhes é criada a partir de uma tabela de exibição e uma implementação **IMAPIProp** . A tabela de exibição descreve a aparência da exibição detalhes e a implementação de **IMAPIProp** controla os dados para o destinatário. Seu provedor é responsável por fornecer a tabela de exibição e a implementação de **IMAPIProp** para cada destinatário. 
  
A maneira mais fácil para criar a tabela de exibição é definir uma estrutura [DTPAGE](dtpage.md) e [BuildDisplayTable](builddisplaytable.md)de chamada. No entanto, alguns provedores, especificamente provedores somente leitura que permitem a criação de destinatários únicos, usam **IPropData**. A implementação de **IMAPIProp** pode ser qualquer tipo de objeto de propriedade. 
  
Há dois métodos para esta caixa de diálogo de invocação: [IAddrBook::Details](iaddrbook-details.md) e [IMAPISupport::Details](imapisupport-details.md). Quando seu provedor chama um destes métodos para solicitar detalhes para um destinatário, MAPI primeiro abre o destinatário chamando o método de [IMAPIContainer::OpenEntry](imapicontainer-openentry.md) do seu contêiner. Em seguida, ele chama o método de [IMAPIProp::OpenProperty](imapiprop-openproperty.md) do destinatário para solicitar a propriedade **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)). **PR_DETAILS_TABLE** é a propriedade que representa a tabela de exibição de detalhes de um destinatário. 
  
O [IPropData: IMAPIProp](ipropdataimapiprop.md) interface pode ser usado para monitorar alterações nos controles de exibição de tabela, conforme descrito no procedimento a seguir. 
  
## <a name="monitor-changes-to-a-control"></a>Monitore as alterações em um controle
  
1. Antes do usuário obtiver acesso ao controle, chame [IPropData::HrSetObjAccess](ipropdata-hrsetobjaccess.md) para definir o acesso do controle como IPROP_CLEAN. 
    
2. Permitir que o usuário trabalhar com a caixa de diálogo. 
    
3. Quando o usuário tiver terminado, chame [IPropData::HrGetPropAccess](ipropdata-hrgetpropaccess.md) para recuperar o nível de acesso atual do controle. 
    
4. Se o nível de acesso for IPROP_DIRTY, o usuário tiver modificado o controle. Seu provedor deve:
    
   - Chame [IPropData::HrSetPropAccess](ipropdata-hrsetpropaccess.md) para definir o acesso do nível de volta ao IPROP_CLEAN. 
    
   - Chame o método de [IMAPIProp::GetProps](imapiprop-getprops.md) do objeto de dados de propriedade para recuperar a propriedade alterada e atualizá-lo chamando [IMAPIProp::SetProps](imapiprop-setprops.md).
    
5. Se o nível de acesso ainda IPROP_CLEAN, o controle não foi modificado. 
    
Para obter mais informações sobre a criação de tabelas de exibição, consulte [Exibir tabelas](display-tables.md).
  

