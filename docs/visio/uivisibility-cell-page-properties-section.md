---
title: Célula UIVisibility (Seção Page Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60090
localization_priority: Normal
ms.assetid: df7f79df-770a-4868-e7e2-05c3828e23eb
description: Determina se o nome da página será exibido na interface do usuário.
ms.openlocfilehash: 51ccd34cb40c286fe6b61818aea5a6b9c0b6d1a4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437326"
---
# <a name="uivisibility-cell-page-properties-section"></a>Célula UIVisibility (Seção Page Properties)

Determina se o nome da página será exibido na interface do usuário.
  
|**Valor**|**Descrição**|**Constante de automação**|
|:-----|:-----|:-----|
|0  <br/> |Exibe o nome da página na interface do usuário (o padrão).  <br/> |**visUIVNormal** <br/> |
|1   <br/> |Não exibe o nome da página na interface do usuário.  <br/> |**visUIVHidden** <br/> |
   
## <a name="remarks"></a>Comentários

A definição da célula UIVisibility como **visUIVHidden** impede que a página seja exibida em qualquer parte da interface do usuário em que a cadeia de caracteres contendo o nome da página apareça. Por exemplo, a página não seria listada como uma opção no **Gerenciador de Desenho** nem nas guias de página. No entanto, a página permanecerá acessível se você usar automação ou caminhos de interface do usuário que não incluam o nome da página, por exemplo, o **comando** Imprimir. 
  
 Essa célula é destinada ao uso com páginas de documento, e não com páginas de sobreposição de marcação, cuja célula UIVisibility é definida como **visUIVHidden** por padrão e não deve ser mudada. 
  
> [!NOTE]
> Para ocultar uma página do  comando Imprimir do documento, torná-la uma página de plano de fundo ( a propriedade **Type** é **visTypeBackground** ) que não é usada como plano de fundo por qualquer página (as formas em páginas de plano de fundo são impressas quando uma página que a utiliza como plano de fundo é impressa). O comando Imprimir **do** documento só funciona com páginas indexadas, e as páginas de plano de fundo não são indexadas. 
  
Para obter uma referência para a célula UIVisibility pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |UIVisibility  <br/> |
   
Para obter uma referência para a célula UIVisibility pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice de linha:  <br/> |**visRowPage** <br/> |
|Índice de célula:  <br/> |**visPageUIVisibility** <br/> |
   

