---
title: Sobre Fórmulas
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm82251823
localization_priority: Normal
ms.assetid: ec0de3e1-21dc-c5d6-2c2a-d5fef80d89bd
description: A chave para controlar ações de forma é gravar fórmulas que definam o comportamento desejado. É possível editar uma fórmula de célula para alterar o valor da célula e, como resultado, modificar um determinado comportamento da forma. Por exemplo, a célula Height da seção Shape Transform contém uma fórmula que pode ser alterada para modificar a altura da forma.
ms.openlocfilehash: e8e1a2b77cc355e930af6f31f0b375dfba321e74
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426258"
---
# <a name="about-formulas"></a>Sobre Fórmulas

A chave para controlar ações de forma é gravar fórmulas que definam o comportamento desejado. É possível editar uma fórmula de célula para alterar o valor da célula e, como resultado, modificar um determinado comportamento da forma. Por exemplo, a célula Height da seção Shape Transform contém uma fórmula que pode ser alterada para modificar a altura da forma.
  
As fórmulas do Microsoft Visio são semelhantes às fórmulas de planilhas comuns em diversos aspectos. O Visio considera tudo na célula, mesmo que seja um valor numérico ou uma simples referência de célula, como uma fórmula.
  
A fórmula em uma célula pode ser herdada da célula equivalente de um mestre ou de um estilo, ou pode ser definida localmente. O Visio avalia a fórmula e converte os resultados para o valor e as unidades apropriados para a célula. Em uma janela do ShapeSheet, você pode exibir o conteúdo da célula como fórmulas ou valores.
  
## <a name="elements-of-a-formula"></a>Elementos de uma fórmula

Uma fórmula sempre começa com um sinal de igual, inserido automaticamente, e pode conter qualquer um dos elementos a seguir:
  
- Números
    
- Coordenadas
    
- Valores booleanos
    
- Operadores
    
- Funções
    
- Cadeias de caracteres
    
- Referências de célula
    
- Unidades de medida
    
## <a name="default-formulas"></a>Fórmulas padrão

Como padrão, quando você cria uma forma, o Visio cria fórmulas para ela. Para ver quais são essas fórmulas padrão, desenhe uma forma simples (como um retângulo, uma elipse ou uma linha reta) e abra sua janela do ShapeSheet (na guia [Desenvolvedor](run-in-developer-mode-display-the-developer-tab.md), clique em **Mostrar ShapeSheet**).
  
## <a name="inherited-formulas"></a>Fórmulas herdadas

O Visio herda as fórmulas sempre que possível. Em vez de fazer uma cópia local de cada fórmula na instância, uma instância herda as fórmulas de seu mestre no estêncil do documento e a formatação da definição de estilo armazenada com o desenho. Esse comportamento resulta em arquivos menores, mas também permite fazer alterações nas fórmulas do mestre ou na definição de estilo para serem propagadas a todas as instâncias.
  
O texto preto em uma célula indica uma fórmula herdada.
  
## <a name="local-formulas"></a>Fórmulas locais

Ao gravar uma fórmula local para uma instância, você está substituindo a fórmula herdada na célula por uma substituição local. Futuras alterações nessa célula no mestre ou no estilo não afetam essa instância porque ela tem uma herança protegida para a célula com a substituição local.
  
A aplicação de um estilo exclui todas as fórmulas locais nas células relacionadas, a menos que você use a função GUARD para protegê-las.
  
O texto azul indica uma fórmula local, que pode ser o resultado da edição da fórmula em uma janela ShapeSheet ou alguma alteração na forma que fez com que o Visio redefinisse a fórmula da célula.
  
## <a name="automatic-updates-to-formulas"></a>Atualizações automáticas das fórmulas

 O Visio atualiza automaticamente determinadas células sempre que uma forma for alterada em um desenho. Isso significa que, em certas circunstâncias, as fórmulas inseridas podem ser substituídas. Por exemplo, se você arrastar a alça do canto para redimensionar uma forma, o Visio redefinirá as fórmulas nas células PinX, PinY, Width e Height. 
  
Se necessário, proteja as fórmulas contra alterações utilizando a função GUARD.
  

