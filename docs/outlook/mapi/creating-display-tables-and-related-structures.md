---
title: Criar tabelas de exibição e estruturas relacionadas
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a8548040-13ed-4a9f-a7ca-de610f94d7df
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 350272324c3827f4630f0cf35e3ade0ff213ac4d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335607"
---
# <a name="creating-display-tables-and-related-structures"></a>Criar tabelas de exibição e estruturas relacionadas
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A criação de uma tabela de exibição é semelhante à gravação de um programa com uma linguagem de script. Você pode criar uma tabela de exibição chamando [BuildDisplayTable](builddisplaytable.md) ou escrevendo código personalizado para preencher as linhas e colunas da tabela. Em geral, você deve usar a técnica **BuildDisplayTable** porque ela é mais simples. 
  
Para que você possa chamar o **BuildDisplayTable** para solicitar MAPI para criar uma tabela de exibição, há uma hierarquia de estruturas que você deve compilar. A estrutura de nível superior, [DTPAGE](dtpage.md), descreve uma única página de propriedades com guias. Em cada estrutura **DTPAGE** é uma estrutura [DTCTL](dtctl.md) que descreve um único controle, como uma caixa de edição ou um botão de opção. Cada estrutura **DTCTL** contém uma estrutura específica para o tipo de controle. Por exemplo, se a estrutura **DTCTL** descreve um controle de caixa de edição, ela conterá uma estrutura **DTBLEDIT** . A estrutura **DTCTL** de um botão de opção contém uma estrutura **DTBLRADIOBUTTON** . 
  
Essas estruturas se relacionam diretamente ao **BuildDisplayTable**; Eles não têm nenhum significado fora do contexto desta função. Ao chamar **BuildDisplayTable**, você passa uma ou mais estruturas **DTPAGE** como parâmetros de entrada. As estruturas **DTPAGE** contêm uma matriz de estruturas **DTCTL** e uma contagem do número de estruturas **DTCTL** na matriz. Há uma estrutura para cada controle a ser exibida na caixa de diálogo. Estruturas **DTPAGE** também têm uma cadeia de caracteres que representa o nome de um arquivo de ajuda correspondente e de um recurso de caixa de diálogo. 
  
Cada estrutura **DTCTL** em uma estrutura **DTPAGE** contém os dados a seguir que são usados para definir propriedades para o controle: 
  
- O tipo de controle para a configuração de **PR_CONTROL_TYPE** ([PidTagControlType](pidtagcontroltype-canonical-property.md)).
    
- Sinalizadores de controle para a configuração de **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)).
    
- Dados de notificação para configuração de **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)).
    
- A estrutura de controle para a configuração de **PR_CONTROL_STRUCTURE** ([PidTagControlStructure](pidtagcontrolstructure-canonical-property.md)).
    
Estruturas **DTCTL** também contêm um identificador de recurso e, para controles de caixa de combinação e edição, um filtro de caractere. 
  
O membro da estrutura de controle de uma estrutura **DTCTL** descreve os dados que são exclusivos para o tipo de controle. MAPI define uma estrutura diferente para cada tipo de controle. Por exemplo, os dados de um controle de edição são representados por uma estrutura **DTBLEDIT** ; os dados de uma caixa de listagem são representados por uma estrutura **DTBLLBX** . 
  
A relação entre os três tipos de estruturas de tabelas de exibição é mostrada na ilustração a seguir. A caixa de diálogo descrita por esta tabela de exibição tem dois controles: um rótulo e um controle de edição. A estrutura **DTBLLBX** tem um membro offset de rótulo, como as várias estruturas de controle, que descrevem onde a cadeia de caracteres do rótulo começa. As cadeias de caracteres de rótulo normalmente são colocadas na memória imediatamente seguinte à estrutura. 
  
**Display table structures**
  
![Exibir estruturas de tabela] (media/dtstruct.gif "Exibir estruturas de tabela")
  
## <a name="see-also"></a>Confira também

- [Implementação da tabela de exibição](display-table-implementation.md)

