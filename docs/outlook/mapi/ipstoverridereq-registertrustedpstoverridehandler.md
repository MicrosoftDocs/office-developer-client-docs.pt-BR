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
description: 'Modificado em: 24 de fevereiro de 2013'
ms.openlocfilehash: acc0986dd80b549b0cb2b941a6937d47a4a959fe
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393870"
---
# <a name="ipstoverridereqregistertrustedpstoverridehandler"></a>IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler

 
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Inicia o procedimento desbloqueando um arquivo de pastas particulares (. pst).
  
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
  
> [in] Um ponteiro para dados de cliente, que serão passados pelo provedor de PST para chamadas subsequentes à função de HrTrustedPSTOverrideHandlerCallback da DLL. Esses dados do cliente podem ser usados pela DLL para auxiliar verificando se o PST deve ser desbloqueado.
    
## <a name="return-value"></a>Valor de retorno

S_OK
  
> A chamada de função foi bem-sucedida.
    
## <a name="remarks"></a>Comentários

A DLL especificada pelo parâmetro wzDllPath deve estar conectada usando um certificado digital. A DLL também deve exportar uma função com a seguinte assinatura.
  
```
extern "C" HRESULT __cdecl HrTrustedPSTOverrideHandlerCallback(IMsgStore *pmstore, IUnknown *pOverride, LPVOID pvClientData)
```

Essa função será chamada com um ponteiro para o objeto IMsgStore para o PST, um ponteiro para um objeto IUnknown que implementa a interface IPSTOVERRIDE1 e um ponteiro para os dados originalmente fornecidos pelo pvClientData.
  
Para obter mais informações, consulte [como implementar um manipulador de substituição de PST para ignorar a política PSTDisableGrow no Outlook 2007](https://support.microsoft.com/kb/956070).
  
## <a name="see-also"></a>Confira também



[IPSTOVERRIDE1 : IUnknown](ipstoverride1iunknown.md)
  
[IPSTOVERRIDEREQ : IUnknown](ipstoverridereqiunknown.md)

