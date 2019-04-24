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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310424"
---
# <a name="showoptions"></a>ShowOptions

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Mostra uma caixa de diálogo modal para coletar informações do usuário. Este ponto de entrada é chamado quando um usuário clica no botão **Opções** ao lado da caixa **tipo de cluster** para o conector de cluster selecionado na caixa de diálogo **Opções do Excel** (na categoria **avançado** abaixo da seção **fórmulas** ). Os conectores de cluster são responsáveis por implementar sua própria interface de caixa de diálogo de opções e para armazenar os dados relacionados no registro ou em qualquer outro lugar. As opções são internas do conector de cluster. O Excel não está ciente delas. 
  
```cpp
int ShowOptions(HWND hWndParent)
```

## <a name="parameters"></a>Parâmetros

_hWndParent_
  
> Uma alça para a janela do Excel.
    
## <a name="return-value"></a>Valor de retorno

**xlHpcRetSuccess** se a caixa de diálogo foi exibida; **xlHpcRetCallFailed** se não foi exibido. 
  
## <a name="remarks"></a>Comentários

Os conectores de cluster podem usar essa caixa de diálogo para obter informações, como qual servidor de cluster usar, do usuário.
  
## <a name="see-also"></a>Confira também

- [Funções de conector de cluster do Excel](excel-cluster-connector-functions.md)

