---
title: ShowOptions
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 51acac58-ec39-488f-979c-1887dc2ab94b
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 5b58b71dc4f2441448eb3e0dac2c3c5763675927
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407694"
---
# <a name="showoptions"></a>ShowOptions

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Mostra uma caixa de diálogo modal para coletar informações do usuário. Esse ponto de entrada é chamado  quando um  usuário clica no botão Opções ao lado da caixa  de tipo cluster para o conector de cluster selecionado na caixa de diálogo Opções do **Excel** (na categoria Avançado na seção **Fórmulas).** Os conectores de cluster são responsáveis por implementar sua própria interface de diálogo de opções e por armazenar os dados relacionados no Registro ou em outro lugar. As opções são internas ao conector do cluster. O Excel não está ciente deles. 
  
```cpp
int ShowOptions(HWND hWndParent)
```

## <a name="parameters"></a>Parâmetros

_hWndParent_
  
> Um alça para a janela do Excel.
    
## <a name="return-value"></a>Valor de retorno

**xlHpcRetSuccess** se a caixa de diálogo foi mostrada; **xlHpcRetCallFailed** se não foi mostrado. 
  
## <a name="remarks"></a>Comentários

Os conectores de cluster podem usar essa caixa de diálogo para obter informações, como qual servidor de cluster usar, do usuário.
  
## <a name="see-also"></a>Confira também

- [Funções de conector de cluster do Excel](excel-cluster-connector-functions.md)

