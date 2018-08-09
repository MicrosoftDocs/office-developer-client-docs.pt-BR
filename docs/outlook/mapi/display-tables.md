---
title: Exibir tabelas
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c314ff6d-3e60-4b81-87ac-6ca6753ff633
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 556d7551f64e075d1f15a945ddb1409c3b5a775f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766458"
---
# <a name="display-tables"></a>Exibir tabelas

  
  
**Aplica-se a**: Outlook 
  
Uma exibição de tabela descreve como mostrar um tipo específico de caixa de diálogo — um tendo uma ou mais páginas com guias Propriedade dedicadas ao exibindo e editando possivelmente uma ou mais propriedades. Associados com cada exibição tabela é um [IMAPIProp: IUnknown](imapipropiunknown.md) implementação de interface. A implementação de **IMAPIProp** mantém os dados de propriedade são apresentados na caixa de diálogo. 
  
As linhas em uma tabela de exibição representam os controles ou objetos de interface do usuário, que são exibidos na caixa de diálogo. MAPI define vários tipos de controles, alguns com valores estáticos e alguns com valores dinâmicos que pode ser alterados por um usuário. A maioria dos controles pode ser associado com propriedades mantidas com a implementação de **IMAPIProp** . Quando um usuário altera o valor de um controle modificável, a propriedade correspondente é atualizada. 
  
Provedores de serviços de implementam as tabelas de exibição e a interface **IMAPIProp** . Criando uma tabela de exibição é semelhante ao escrever um programa com uma linguagem de script. Provedores de serviços podem criar uma tabela de exibição por: 
  
- Chamar a função de [BuildDisplayTable](builddisplaytable.md) . 
    
    - Ou -
    
- Incluindo um código personalizado que preenche a tabela de exibição diretamente usando um objeto de dados de tabela — um objeto que dá suporte a [ITableData: IUnknown](itabledataiunknown.md) interface. 
    
A função **BuildDisplayTable** combine informações de estruturas de tabela de exibição com elementos visuais de um recurso de caixa de diálogo Criar exibição linhas da tabela. A função retorna um ponteiro para uma [IMAPITable: IUnknown](imapitableiunknown.md) interface implementação e, se solicitado, um ponteiro para uma implementação de interface **ITableData** . 
  
Usando o **BuildDisplayTable** para criar uma tabela de exibição é simples e facilita a manutenção quando alterar elementos visuais da tela. No entanto, os provedores de serviços que preferem não usar **BuildDisplayTable** podem criar uma tabela de exibição com código personalizado que usa os métodos de **ITableData**. Por exemplo, provedores de serviço que possuírem uma estrutura de modelo existente para suas páginas de propriedades talvez queira criar um código personalizado em vez de usar **BuildDisplayTable**.
  
Há várias maneiras de provedores de serviços podem implementar a interface de propriedade para sua tabela de exibição. Elas incluem:
  
- Fornecendo um padrão [IMAPIProp: IUnknown](imapipropiunknown.md) implementação. 
    
- Fornecendo uma implementação **IMAPIProp** com quebra que inclui o processamento especial antes de fazer as chamadas padrão. 
    
- Fornecendo uma [IPropData: IMAPIProp](ipropdataimapiprop.md) implementação. 
    
O tipo de implementação depende as características dos dados a ser exibido e o provedor de serviço responsável. Por exemplo, se houver uma relação implícita entre os dados em dois controles de edição e um dos controles é alterado, a implementação de **IMAPIProp** deverá alterar o valor de outro controle apropriadamente. 
  
Tabelas de exibição têm as seguintes propriedades no seu conjunto de coluna necessária:
  
|||
|:-----|:-----|
|**PR_XPOS** ([PidTagXCoordinate](pidtagxcoordinate-canonical-property.md))  <br/> |**PR_YPOS** ([PidTagYCoordinate](pidtagycoordinate-canonical-property.md))  <br/> |
|**PR_DELTAX** ([PidTagDeltaX](pidtagdeltax-canonical-property.md))  <br/> |**PR_DELTAY** ([PidTagDeltaY](pidtagdeltay-canonical-property.md))  <br/> |
|**PR_CONTROL_TYPE** ([PidTagControlType](pidtagcontroltype-canonical-property.md))  <br/> |**PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md))  <br/> |
|**PR_CONTROL_STRUCTURE** ([PidTagControlStructure](pidtagcontrolstructure-canonical-property.md))  <br/> |**PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md))  <br/> |
   
 **PR_XPOS** e **PR_YPOS** especificam as coordenadas X e Y do canto superior esquerdo do controle. As unidades horizontais são 1/4 da unidade base largura diálogo; as unidades verticais são 1/8 da unidade base altura diálogo. Windows computa as unidades base do diálogo atual da altura e largura da fonte do sistema atual. As coordenadas são em relação à origem da área de página de propriedade. O tamanho das páginas de propriedade é limitado para unidades de diálogo de 200 por 180 aproximadamente. 
  
 **PR_DELTAX** e **PR_DELTAY** são a largura e altura do controle. Estes são os valores ULONG. As unidades de largura são 1/4 da unidade base largura diálogo; as unidades de altura são 1/8 da unidade base altura diálogo. As coordenadas são em relação à origem do controle. 
  
As quatro propriedades descrevem várias características do controle. **PR_CONTROL_TYPE** indica o tipo de controle. MAPI define doze tipos de controles, cada um com um conjunto diferente de atributos. Esses atributos são descritos na propriedade flags, **PR_CONTROL_FLAGS**. Se um controle é editável ou necessária ou não são exemplos de atributos. 
  
A estrutura de controle, **PR_CONTROL_STRUCTURE**, contém informações relevantes para o tipo específico de controle. Cada tipo de controle é descrito com uma estrutura diferente. Por exemplo, os controles de edição são descritos com a estrutura [DTBLEDIT](dtbledit.md) . Estruturas **DTBLEDIT** contêm membros dessa lista o número de e tipos específicos de caracteres que podem ser colocados no controle e uma marca de propriedade que identifica a propriedade cujo valor deve ser exibida no controle. **PR_CONTROL_STRUCTURE** é armazenada como uma propriedade binária. 
  
O identificador de controle, **PR_CONTROL_ID**, identifica exclusivamente o controle de caixa de diálogo descrito pela tabela de exibição. **PR_CONTROL_ID** é definido por valores colocados nos membros *lpbNotif* e *cbNotif* da estrutura [DTCTL](dtctl.md) que é usado pelo **BuildDisplayTable** para criar a tabela de exibição. Porque o MAPI às vezes combina as tabelas de exibição, o identificador de **PR_CONTROL_ID** deve sempre ser exclusivo. Normalmente, provedores atribuem uma estrutura [GUID](guid.md) **PR_CONTROL_ID** para garantir que sua exclusividade. A propriedade **PR_CONTROL_ID** está incluída na estrutura [TABLE_NOTIFICATION](table_notification.md) quando uma notificação de tabela de exibição é gerada. 
  
Para obter mais informações sobre tabelas de exibição, consulte [Sobre notificações de tabela de exibir](about-display-table-notifications.md)e [Implementação de tabela exibir](display-table-implementation.md) . 
  
## <a name="see-also"></a>Confira também



[Tabelas MAPI](mapi-tables.md)

