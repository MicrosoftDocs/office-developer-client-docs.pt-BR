---
title: ShowOptions
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 51acac58-ec39-488f-979c-1887dc2ab94b
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: dbf6f0f50e9f7fa988e83f3b58012e9deac13eac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765437"
---
# <a name="showoptions"></a>ShowOptions

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Mostra a caixa de diálogo modal para coletar informações do usuário. Esse ponto de entrada é chamado quando um usuário clica no botão de **Opções** ao lado da caixa **tipo de Cluster** para o conector de cluster selecionado na caixa de diálogo **Opções do Excel** (na categoria **Avançado** sob a seção de **fórmulas** ). Conectores de cluster são responsáveis para implementar sua própria interface de diálogo Opções e para armazenar os dados relacionados no registro ou em outro local. As opções são internas para o conector de cluster. Excel não está ciente deles. 
  
```cpp
int ShowOptions(HWND hWndParent)
```

## <a name="parameters"></a>Par�metros

_hWndParent_
  
> Um identificador para a janela do Excel.
    
## <a name="return-value"></a>Valor retornado

**xlHpcRetSuccess** se a caixa de diálogo foi mostrada; **xlHpcRetCallFailed** se ele não foi exibido. 
  
## <a name="remarks"></a>Coment�rios

Conectores de cluster podem usar esta caixa de diálogo para obter mais informações, como o que o servidor do cluster use, do usuário.
  
## <a name="see-also"></a>Confira também

- [Funções de conector de Cluster do Excel](excel-cluster-connector-functions.md)

