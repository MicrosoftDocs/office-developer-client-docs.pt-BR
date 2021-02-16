---
title: IPSTOVERRIDEREQRegisterTrustedPSTOverrideHandler
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTOVERRIDEREQ.RegisterTrustedPSTOverrideHandler
api_type:
- COM
ms.assetid: 4a73c77c-7e32-4302-bffe-a1ea13574731
description: 'Última modificação: 24 de fevereiro de 2013'
ms.openlocfilehash: acc0986dd80b549b0cb2b941a6937d47a4a959fe
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279532"
---
# <a name="ipstoverridereqregistertrustedpstoverridehandler"></a>IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler

 
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Inicia o procedimento de desbloqueio para um arquivo de Pastas Particulares (.pst).
  
```cpp
HRESULT RegisterTrustedPSTOverrideHandler (
  LPCWSTR pwzDllPath, 
  LPVOID pvClientData
); 

```

## <a name="parameters"></a>Parâmetros

 _pwzDllPath_
  
> [in] Um ponteiro para o caminho de uma biblioteca de vínculo dinâmico (DLL) de terceiros.
    
 _pvClientData_
  
> [in] Um ponteiro para os dados do cliente, que será passado pelo provedor PST para chamadas subsequentes para a função HrTrustedPSTOverrideHandlerCallback da DLL. Esses dados de cliente podem ser usados pela DLL para ajudar a verificar se o PST deve ser desbloqueado.
    
## <a name="return-value"></a>Valor de retorno

S_OK
  
> A chamada de função foi bem-sucedida.
    
## <a name="remarks"></a>Comentários

A DLL especificada pelo parâmetro wzDllPath deve ser assinada usando um certificado digital. A DLL também deve exportar uma função com a assinatura a seguir.
  
```
extern "C" HRESULT __cdecl HrTrustedPSTOverrideHandlerCallback(IMsgStore *pmstore, IUnknown *pOverride, LPVOID pvClientData)
```

Essa função será chamada com um ponteiro para o objeto IMsgStore para o PST, um ponteiro para um objeto IUnknown que implementa a interface IPSTOVERRIDE1 e um ponteiro para os dados originalmente fornecidos por meio de pvClientData.
  
For more information see [How to implement a PST override handler to bypass the PSTDisableGrow policy in Outlook 2007](https://support.microsoft.com/kb/956070).
  
## <a name="see-also"></a>Confira também



[IPSTOVERRIDE1 : IUnknown](ipstoverride1iunknown.md)
  
[IPSTOVERRIDEREQ : IUnknown](ipstoverridereqiunknown.md)

