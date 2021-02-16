---
title: Exibir Tabelas
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c314ff6d-3e60-4b81-87ac-6ca6753ff633
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 1b94b0ea69237be3675e1ea02fc3e2bfac337025
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406217"
---
# <a name="display-tables"></a>Exibir Tabelas

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A display table describes how to show a specific type of dialog box one having one or more tabbed property pages dedicated to displaying and possibly editing one or more properties. Associado a cada tabela de exibição é uma [implementação de interface IMAPIProp : IUnknown.](imapipropiunknown.md) A **implementação de IMAPIProp** mantém os dados de propriedade apresentados na caixa de diálogo. 
  
As linhas em uma tabela de exibição representam os controles, ou objetos de interface do usuário, que são exibidos na caixa de diálogo. MAPI define muitos tipos de controles, alguns com valores estáticos e outros com valores dinâmicos que um usuário pode alterar. A maioria dos controles pode ser associada a propriedades mantidas com a **implementação IMAPIProp.** Quando um usuário altera o valor de um controle modificável, a propriedade correspondente é atualizada. 
  
Os provedores de serviços implementam tabelas de exibição e a interface **IMAPIProp.** Criar uma tabela de exibição é semelhante a escrever um programa com uma linguagem de script. Os provedores de serviços podem criar uma tabela de exibição ao: 
  
- Chamando a [função BuildDisplayTable.](builddisplaytable.md) 
    
    - Ou -
    
- Incluindo código personalizado que preenche a tabela de exibição diretamente usando um objeto de dados de tabela — um objeto que dá suporte à interface [ITableData : IUnknown.](itabledataiunknown.md) 
    
A **função BuildDisplayTable** combina informações de estruturas de tabela de exibição com elementos visuais de um recurso de caixa de diálogo para criar linhas de tabela de exibição. A função retorna um ponteiro para uma [IMAPITable :](imapitableiunknown.md) implementação de interface IUnknown e, se solicitado, um ponteiro para uma implementação de interface **ITableData.** 
  
Usar **BuildDisplayTable para** criar uma tabela de exibição é simples e facilita a manutenção quando os elementos visuais da exibição mudam. No entanto, os provedores de serviços que preferem não usar **BuildDisplayTable** podem criar uma tabela de exibição com código personalizado que usa os métodos de **ITableData**. Por exemplo, os provedores de serviços que têm uma estrutura de modelo existente para suas páginas de propriedades podem querer criar código personalizado em vez de usar **BuildDisplayTable**.
  
Há várias maneiras de os provedores de serviços implementarem a interface de propriedade para sua tabela de exibição. Entre eles:
  
- Fornecimento de uma [implementação IMAPIProp padrão: IUnknown.](imapipropiunknown.md) 
    
- Fornecer uma implementação **IMAPIProp empacotada** que inclui processamento especial antes de fazer as chamadas padrão. 
    
- Fornecendo uma [implementação IPropData : IMAPIProp.](ipropdataimapiprop.md) 
    
O tipo de implementação depende das características dos dados a serem exibidos e do provedor de serviços responsável. Por exemplo, se houver uma relação implícita entre os dados em dois controles de edição e um dos controles mudar, a implementação **de IMAPIProp** deverá alterar o valor do outro controle adequadamente. 
  
As tabelas de exibição têm as seguintes propriedades em seu conjunto de colunas obrigatório:
  
|||
|:-----|:-----|
|**PR_XPOS** ([PidTagXCoordinate](pidtagxcoordinate-canonical-property.md))  <br/> |**PR_YPOS** ([PidTagYCoordinate](pidtagycoordinate-canonical-property.md))  <br/> |
|**PR_DELTAX** ([PidTagDeltaX](pidtagdeltax-canonical-property.md))  <br/> |**PR_DELTAY** ([PidTagDeltaY](pidtagdeltay-canonical-property.md))  <br/> |
|**PR_CONTROL_TYPE** ([PidTagControlType](pidtagcontroltype-canonical-property.md))  <br/> |**PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md))  <br/> |
|**PR_CONTROL_STRUCTURE** ([PidTagControlStructure](pidtagcontrolstructure-canonical-property.md))  <br/> |**PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md))  <br/> |
   
 **PR_XPOS** e **PR_YPOS** as coordenadas X e Y do canto superior esquerdo do controle. As unidades horizontais são 1/4 da unidade de largura base da caixa de diálogo; as unidades verticais são 1/8 da unidade de altura base da caixa de diálogo. O Windows calcula as unidades base atuais da caixa de diálogo a partir da altura e da largura da fonte atual do sistema. As coordenadas são relativas à origem da área da página de propriedades. O tamanho das páginas de propriedades é limitado a aproximadamente 200 por 180 unidades de diálogo. 
  
 **PR_DELTAX** e **PR_DELTAY** são a largura e a altura do controle. Esses são valores ULONG. As unidades de largura são 1/4 da unidade de largura base da caixa de diálogo; as unidades de altura são 1/8 da unidade de altura base da caixa de diálogo. As coordenadas são relativas à origem do controle. 
  
As outras quatro propriedades descrevem várias características do controle. **PR_CONTROL_TYPE** indica o tipo de controle. MAPI define doze tipos de controles, cada um com um conjunto diferente de atributos. Esses atributos são descritos na propriedade flags, **PR_CONTROL_FLAGS**. Exemplos de atributos incluem se um controle é editável ou obrigatório. 
  
A estrutura de controle, **PR_CONTROL_STRUCTURE**, contém informações relevantes para o tipo específico de controle. Cada tipo de controle é descrito com uma estrutura diferente. Por exemplo, os controles de edição são descritos com a [estrutura DTBLEDIT.](dtbledit.md) Estruturas **DTBLEDIT** contêm membros que listam o número e tipos específicos de caracteres que podem ser colocados no controle e uma marca de propriedade que identifica a propriedade cujo valor deve ser exibido no controle. **PR_CONTROL_STRUCTURE** é armazenado como uma propriedade binária. 
  
O identificador de controle, **PR_CONTROL_ID**, identifica exclusivamente o controle na caixa de diálogo descrita pela tabela de exibição. **PR_CONTROL_ID** é definido a partir dos valores colocados nos membros  *lpbNotif*  e  *cbNotif*  da estrutura [DTCTL](dtctl.md) usada por **BuildDisplayTable** para criar a tabela de exibição. Como o MAPI às vezes combina tabelas de exibição, o identificador **PR_CONTROL_ID** deve ser sempre exclusivo. Normalmente, os provedores atribuem uma [estrutura GUID](guid.md) PR_CONTROL_ID **para** garantir sua exclusividade. A **PR_CONTROL_ID** propriedade é incluída na estrutura [TABLE_NOTIFICATION](table_notification.md) quando uma notificação de tabela de exibição é gerada. 
  
Para obter mais informações sobre tabelas de exibição, consulte Implementação da tabela de [exibição](display-table-implementation.md) e [sobre notificações de tabela de exibição.](about-display-table-notifications.md) 
  
## <a name="see-also"></a>Confira também



[Tabelas MAPI](mapi-tables.md)

