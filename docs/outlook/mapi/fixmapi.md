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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383811"
---
# <a name="fixmapi"></a>FixMAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Faz uma cópia de backup da cópia atual do MAPI32 no cliente, computador e restaura Mapi32 com a biblioteca stub MAPI, Mapistub.
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Exportá-los por:  <br/> |Mapistub  <br/> |
|Chamado por:  <br/> |Cliente  <br/> |
|Implementado por:  <br/> |Windows  <br/> |
   
```cpp
DWORD STDAPICALLTYPE FixMAPI(void); 
```

## <a name="return-values"></a>Valores de retorno

Se a função tiver êxito, o valor de retorno é um valor diferente de zero.
  
Se a função falhar, o valor de retorno é zero. Para obter informações de erro estendidas, chame a função de Software Development Kit (SDK) do Microsoft Windows, **[GetLastError](https://msdn.microsoft.com/library/ms679360.aspx)**. 
  
## <a name="remarks"></a>Comentários

 **FixMAPI** não substitui o arquivo Mapi32 atual se o arquivo está marcado como somente leitura. 
  
 **FixMAPI** não substitui o Mapi32 atual se o Microsoft Exchange Server estiver instalado no computador. 
  
Quando **FixMAPI** faz uma cópia de backup da cópia atual do MAPI32 no computador, ele atribui a cópia de backup um nome diferente do "Mapi32". Ele, em seguida, direciona as chamadas subsequentes destinadas a nesse assembly para a cópia de backup. 
  
## <a name="see-also"></a>Confira também



[KB 256946: Você recebe uma mensagem de erro de conflito do programa quando você inicia o Outlook 2000](https://support.microsoft.com/kb/256946)
  
[KB 228457: Descrição da ferramenta Fixmapi.exe incluída com o Internet Explorer 5](https://support.microsoft.com/kb/228457)

