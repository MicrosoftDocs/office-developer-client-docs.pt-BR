---
title: Criando tabelas de exibição e estruturas relacionadas
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a8548040-13ed-4a9f-a7ca-de610f94d7df
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 177fe21537e921a4b94a34ad531847701b16c344
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766350"
---
# <a name="creating-display-tables-and-related-structures"></a>Criando tabelas de exibição e estruturas relacionadas
  
**Aplica-se a**: Outlook 
  
Criando uma tabela de exibição é semelhante ao escrever um programa com uma linguagem de script. Você pode criar uma tabela de exibição por chamar [BuildDisplayTable](builddisplaytable.md) ou escrever o código personalizado para preencher as linhas e colunas da tabela. Em geral, você deve usar a técnica **BuildDisplayTable** porque ele é mais simples. 
  
Antes de chamar **BuildDisplayTable** para solicitar que o MAPI para criar uma exibição de tabela, há uma hierarquia de estruturas que você deve construir. A estrutura de nível superior, [DTPAGE](dtpage.md), descreve uma página de propriedades com guias único. Em cada **DTPAGE** estrutura é uma estrutura [DTCTL](dtctl.md) que descreve um controle exclusivo, como uma caixa de edição ou um botão de opção. Cada estrutura **DTCTL** contém uma estrutura que é específica para o tipo de controle. Por exemplo, se a estrutura **DTCTL** descreve um controle de caixa de edição, ele irá conter uma estrutura **DTBLEDIT** . A estrutura **DTCTL** para um botão de opção contém uma estrutura **DTBLRADIOBUTTON** . 
  
Essas estruturas se relacionam diretamente com **BuildDisplayTable**; eles não têm significado fora do contexto dessa função. Quando você chama **BuildDisplayTable**, você passa uma ou mais estruturas **DTPAGE** como parâmetros de entrada. As estruturas **DTPAGE** contenham uma matriz de estruturas **DTCTL** e uma contagem do número de estruturas **DTCTL** na matriz. Não há uma estrutura para cada controle a ser exibido na caixa de diálogo. Estruturas **DTPAGE** também têm uma cadeia de caracteres que representa o nome de um correspondente ajuda arquivo e caixa de diálogo caixa recurso. 
  
Cada estrutura **DTCTL** em uma estrutura **DTPAGE** contém os seguintes dados que são usados para definir propriedades para o controle: 
  
- O tipo de controle para a configuração **PR_CONTROL_TYPE** ([PidTagControlType](pidtagcontroltype-canonical-property.md)).
    
- Sinalizadores de controle para a configuração **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)).
    
- Dados de notificação para a definição de **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)).
    
- A estrutura de controle para a definição de **PR_CONTROL_STRUCTURE** ([PidTagControlStructure](pidtagcontrolstructure-canonical-property.md)).
    
Estruturas **DTCTL** também contenham um identificador de recurso e, para editar e controles de caixa de combinação, um filtro de caractere. 
  
O membro de estrutura de controle de uma estrutura **DTCTL** descreve os dados que seja exclusivos para o tipo de controle. MAPI define uma estrutura diferente para cada tipo de controle. Por exemplo, os dados de um controle de edição são representados por uma estrutura **DTBLEDIT** ; os dados de uma caixa de listagem são representados por uma estrutura **DTBLLBX** . 
  
A relação entre os três tipos de estruturas de tabela de exibição é mostrada na ilustração a seguir. A caixa de diálogo descrita pela tabela exibição tem dois controles: um rótulo e um controle de edição. A estrutura **DTBLLBX** tem um membro de deslocamento de rótulo, como várias das estruturas de controle, que descreve onde a cadeia de caracteres para o rótulo começa. Cadeias de caracteres de rótulo geralmente são colocadas na memória imediatamente após a estrutura. 
  
**Exibir estruturas de tabela**
  
![Estruturas de tabela de exibição] (media/dtstruct.gif "Estruturas de tabela de exibição")
  
## <a name="see-also"></a>Confira também

- [Implementação da tabela de exibição](display-table-implementation.md)

