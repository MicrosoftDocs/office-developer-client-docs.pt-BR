---
title: FixMAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 32676003-ba32-886f-1185-4760cb0e30e3
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 2aeca1a65a859ac9502995a463bc4869609bcd15
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334958"
---
# <a name="fixmapi"></a>FixMAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Faz uma cópia de backup da cópia atual mapi32.dll no computador cliente e restaura mapi32.dll com a biblioteca stub MAPI, mapistub.dll.
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Exportado por:  <br/> |mapistub.dll  <br/> |
|Chamado por:  <br/> |Cliente  <br/> |
|Implementado por:  <br/> |Windows  <br/> |
   
```cpp
DWORD STDAPICALLTYPE FixMAPI(void); 
```

## <a name="return-values"></a>Valor de retorno

Se a função for bem-sucedida, o valor de retorno será um valor não zero.
  
Se a função falhar, o valor de retorno será zero. Para obter informações de erro estendidas, chame a função Microsoft Windows Software Development Kit (SDK), **[GetLastError](https://msdn.microsoft.com/library/ms679360.aspx)**. 
  
## <a name="remarks"></a>Comentários

 **FixMAPI** não substituirá o arquivo mapi32.dll atual se o arquivo estiver marcado como somente leitura. 
  
 **FixMAPI** não substitui o mapi32.dll atual se o Microsoft Exchange Server estiver instalado no computador. 
  
Quando **FixMAPI** faz uma cópia de backup da cópia atual mapi32.dll no computador, ele atribui à cópia de backup um nome diferente de "mapi32.dll". Em seguida, ele direciona chamadas subsequentes destinadas a esse assembly para a cópia de backup. 
  
## <a name="see-also"></a>Confira também



[KB 256946: Você recebe uma mensagem de erro de conflito de programa ao iniciar o Outlook 2000](https://support.microsoft.com/kb/256946)
  
[KB 228457: Descrição da ferramenta Fixmapi.exe incluída com o Internet Explorer 5](https://support.microsoft.com/kb/228457)

