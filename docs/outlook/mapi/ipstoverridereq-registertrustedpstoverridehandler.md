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
ms.openlocfilehash: 4fc3b7427fc13a024aab38c7b7df1d940a4730ac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767678"
---
# <a name="ipstoverridereqregistertrustedpstoverridehandler"></a>IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler

 
  
**Aplica-se a**: Outlook 
  
Inicia o procedimento desbloqueando um arquivo de pastas particulares (. pst).
  
```cpp
HRESULT RegisterTrustedPSTOverrideHandler (
  LPCWSTR pwzDllPath, 
  LPVOID pvClientData
); 

```

## <a name="parameters"></a>Par�metros

 _pwzDllPath_
  
> [in] Um ponteiro para o caminho de uma biblioteca de vínculo dinâmico (DLL) de terceiros.
    
 _pvClientData_
  
> [in] Um ponteiro para dados de cliente, que serão passados pelo provedor de PST para chamadas subsequentes à função de HrTrustedPSTOverrideHandlerCallback da DLL. Esses dados do cliente podem ser usados pela DLL para auxiliar verificando se o PST deve ser desbloqueado.
    
## <a name="return-value"></a>Valor retornado

S_OK
  
> A chamada de função foi bem-sucedida.
    
## <a name="remarks"></a>Coment�rios

A DLL especificada pelo parâmetro wzDllPath deve estar conectada usando um certificado digital. A DLL também deve exportar uma função com a seguinte assinatura.
  
```
extern "C" HRESULT __cdecl HrTrustedPSTOverrideHandlerCallback(IMsgStore *pmstore, IUnknown *pOverride, LPVOID pvClientData)
```

Essa função será chamada com um ponteiro para o objeto IMsgStore para o PST, um ponteiro para um objeto IUnknown que implementa a interface IPSTOVERRIDE1 e um ponteiro para os dados originalmente fornecidos pelo pvClientData.
  
Para obter mais informações, consulte [como implementar um manipulador de substituição de PST para ignorar a política PSTDisableGrow no Outlook 2007](http://support.microsoft.com/kb/956070).
  
## <a name="see-also"></a>Confira também



[IPSTOVERRIDE1: IUnknown](ipstoverride1iunknown.md)
  
[IPSTOVERRIDEREQ: IUnknown](ipstoverridereqiunknown.md)

