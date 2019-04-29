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
ms.openlocfilehash: 1b94b0ea69237be3675e1ea02fc3e2bfac337025
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406217"
---
# <a name="display-tables"></a>Exibir tabelas

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Uma tabela de exibição descreve como mostrar um tipo específico de caixa de diálogo — uma ou mais páginas de propriedades com guias dedicadas para exibir e possivelmente editar uma ou mais propriedades. Associado a cada tabela de exibição é uma implementação de interface [IMAPIProp: IUnknown](imapipropiunknown.md) . A implementação do **IMAPIProp** mantém os dados de propriedade apresentados na caixa de diálogo. 
  
As linhas em uma tabela de exibição representam os controles, ou objetos da interface do usuário, que são exibidos na caixa de diálogo. O MAPI define vários tipos de controles, alguns com valores estáticos e alguns com valores dinâmicos que um usuário pode alterar. A maioria dos controles pode ser associada às propriedades mantidas com a implementação **IMAPIProp** . Quando um usuário altera o valor de um controle modificável, a propriedade correspondente é atualizada. 
  
Os provedores de serviços implementam tabelas de exibição e a interface **IMAPIProp** . A criação de uma tabela de exibição é semelhante à gravação de um programa com uma linguagem de script. Os provedores de serviços podem criar uma tabela de exibição por: 
  
- Chamar a função [BuildDisplayTable](builddisplaytable.md) . 
    
    - Ou
    
- Incluindo o código personalizado que preenche a tabela de exibição diretamente usando um objeto Table Data — um objeto que dá suporte à interface [ITableData: IUnknown](itabledataiunknown.md) . 
    
A função **BuildDisplayTable** combina informações de estruturas de tabelas de exibição com elementos visuais de um recurso de caixa de diálogo para compilar linhas de tabela de exibição. A função retorna um ponteiro para uma implementação de interface imApitable [: IUnknown](imapitableiunknown.md) e, se solicitado, um ponteiro para uma implementação de interface **ITableData** . 
  
O uso do **BuildDisplayTable** para criar uma tabela de exibição é simples e torna a manutenção mais fácil quando os elementos visuais da exibição mudam. No enTanto, os provedores de serviços que preferem não usar o **BuildDisplayTable** podem criar uma tabela de exibição com código personalizado que usa os métodos de **ITableData**. Por exemplo, os provedores de serviços que têm uma estrutura de modelo existente para suas páginas de propriedades podem querer criar código personalizado em vez de usar **BuildDisplayTable**.
  
Há várias maneiras pelas quais os provedores de serviços podem implementar a interface de propriedade para a tabela de exibição. Entre eles:
  
- Fornecer uma implementação [IMAPIProp: IUnknown](imapipropiunknown.md) padrão. 
    
- Fornecer uma implementação de **IMAPIProp** encapsulada que inclui processamento especial antes de fazer as chamadas padrão. 
    
- Fornecer uma implementação de [IPropData: IMAPIProp](ipropdataimapiprop.md) . 
    
O tipo de implementação depende das características dos dados a serem exibidos e do provedor de serviços responsáveis. Por exemplo, se houver um relacionamento implícito entre os dados de dois controles de edição e um dos controles mudar, a implementação **IMAPIProp** deve alterar o valor do outro controle adequadamente. 
  
As tabelas de exibição têm as seguintes propriedades no conjunto de colunas exigido:
  
|||
|:-----|:-----|
|**PR_XPOS** ([PidTagXCoordinate](pidtagxcoordinate-canonical-property.md))  <br/> |**PR_YPOS** ([PidTagYCoordinate](pidtagycoordinate-canonical-property.md))  <br/> |
|**PR_DELTAX** ([PidTagDeltaX](pidtagdeltax-canonical-property.md))  <br/> |**PR_DELTAY** ([PidTagDeltaY](pidtagdeltay-canonical-property.md))  <br/> |
|**PR_CONTROL_TYPE** ([PidTagControlType](pidtagcontroltype-canonical-property.md))  <br/> |**PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md))  <br/> |
|**PR_CONTROL_STRUCTURE** ([PidTagControlStructure](pidtagcontrolstructure-canonical-property.md))  <br/> |**PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md))  <br/> |
   
 **PR_XPOS** e **PR_YPOS** especificam as coordenadas X e Y do canto superior esquerdo do controle. As unidades horizontais são 1/4 da unidade de largura de base da caixa de diálogo; as unidades verticais são 1/8 da unidade de altura da base da caixa de diálogo. O Windows calcula as unidades base da caixa de diálogo atual da altura e da largura da fonte atual do sistema. As coordenadas são relativas à origem da área da página de propriedades. O tamanho das páginas de propriedades está limitado a aproximadamente 200 por unidades de caixa de diálogo de 180. 
  
 **PR_DELTAX** e **PR_DELTAY** são a largura e a altura do controle. Estes são valores ULONG. As unidades de largura são 1/4 da unidade de largura de base da caixa de diálogo; as unidades de altura são 1/8 da unidade de altura da base da caixa de diálogo. As coordenadas são relativas à origem do controle. 
  
As outras quatro propriedades descrevem várias características do controle. **PR_CONTROL_TYPE** indica o tipo de controle. O MAPI define doze tipos de controles, cada um com um conjunto diferente de atributos. Esses atributos são descritos na Propriedade Flags, **PR_CONTROL_FLAGS**. Exemplos de atributos incluem se um controle é ou não editável ou obrigatório. 
  
A estrutura de controle, **PR_CONTROL_STRUCTURE**, contém informações relevantes para o tipo de controle específico. Cada tipo de controle é descrito com uma estrutura diferente. Por exemplo, os controles de edição são descritos com a estrutura [DTBLEDIT](dtbledit.md) . Estruturas **DTBLEDIT** contêm membros que listam o número de caracteres e tipos específicos que podem ser colocados no controle e uma marca de propriedade que identifica a propriedade cujo valor deve ser exibido no controle. **PR_CONTROL_STRUCTURE** é armazenado como uma propriedade binária. 
  
O identificador de controle, **PR_CONTROL_ID**, identifica exclusivamente o controle na caixa de diálogo descrita pela tabela de exibição. **PR_CONTROL_ID** é definido a partir dos valores colocados nos membros *lpbNotif* e *cbNotif* da estrutura [DTCTL](dtctl.md) que é usada pelo **BuildDisplayTable** para criar a tabela de exibição. Como o MAPI, às vezes, combina tabelas de exibição, o identificador no **PR_CONTROL_ID** deve sempre ser exclusivo. Normalmente, os provedores atribuem uma estrutura [GUID](guid.md) a **PR_CONTROL_ID** para garantir sua exclusividade. A propriedade **PR_CONTROL_ID** é incluída na estrutura [TABLE_NOTIFICATION](table_notification.md) quando uma notificação de tabela de exibição é gerada. 
  
Para obter mais informações sobre as tabelas de exibição, consulte [exibir a implementação da tabela](display-table-implementation.md) e [sobre exibir notificações de tabela](about-display-table-notifications.md). 
  
## <a name="see-also"></a>Confira também



[Tabelas MAPI](mapi-tables.md)

