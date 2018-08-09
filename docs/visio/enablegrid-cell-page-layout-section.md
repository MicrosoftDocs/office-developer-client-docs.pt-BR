---
title: Célula EnableGrid (Seção Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251642
localization_priority: Normal
ms.assetid: bfea4ef4-1b30-eb22-215d-3b9b73098da9
description: Determina se o aplicativo dispõe as formas com base em uma grade de página interna e invisível quando você configura o layout na caixa de diálogo Configurar Layout. (Na guia Design, no grupo Layout, clique em Refazer o Layout da Página e clique em Opções de Layout).
ms.openlocfilehash: 3371767343132219ebc38134b93afd1da46c7a45
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771797"
---
# <a name="enablegrid-cell-page-layout-section"></a>Célula EnableGrid (Seção Page Layout)

Determina se o aplicativo dispõe as formas com base em uma grade de página interna e invisível quando você configura o layout na caixa de diálogo **Configurar Layout**. (Na guia **Design**, no grupo **Layout**, clique em **Refazer o Layout da Página** e clique em **Opções de Layout**).
  
|**Valor**|**Descrição**|
|:-----|:-----|
|VERDADEIRO  <br/> |Utilizar a grade de página interna.  <br/> |
|FALSO  <br/> |Não utilizar a grade de página interna.  <br/> |
   
## <a name="remarks"></a>Comentários

Você cria essa grade de página, usando os valores de **Espaço entre formas** e **Tamanho médio da forma** na caixa de diálogo **Espaçamento de Layout e Direcionamento**. (Na guia **Design**, clique na seta **Configurar Página**, clique em **Layout e Direcionamento** e clique em **Espaçamento**.) 
  
Ao ativar esse recurso, o aplicativo alinha cada ponto central da forma de colocação com o centro de um bloco na grade de página interna. 
  
Para obter uma referência para a célula EnableGrid pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |EnableGrid  <br/> |
   
Para obter uma referência para a célula EnableGrid pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice da linha:  <br/> |**visRowPageLayout** <br/> |
|Índice da célula:  <br/> |**visPLOEnableGrid** <br/> |
   

