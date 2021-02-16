---
title: IPSTOVERRIDE1SetPersistedRegistrations
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTOVERRIDE1.SetPersistedRegistrations
api_type:
- COM
ms.assetid: 5f4b62db-a759-41a2-9bea-29fc04b2962b
description: 'Last modified: November 08, 2011'
ms.openlocfilehash: 6583765d4df7c7bfae9e7a62606beaa857874954
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408345"
---
# <a name="ipstoverride1setpersistedregistrations"></a>IPSTOVERRIDE1::SetPersistedRegistrations

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Registra arquivos de Pastas Particulares (.pst) para desbloqueio automático, evitando mais chamadas para o HrTrustedPSTOverrideHandlerCallback.
  
```cpp
HRESULT SetPersistedRegistrations(
  SPropValue *pmval
);
```

## <a name="parameters"></a>Parâmetros

_pmval_
  
> [in] Uma [estrutura SPropValue](spropvalue.md) que contém um ponteiro para o caminho da biblioteca de vínculo dinâmico (DLL) a ser registrado. A estrutura tem as seguintes características: 
    
   - Uma ulPropTag de [PROP_TAG](prop_tag.md)(PT_MV_UNICODE, PROP_ID_NULL).
    
   - Uma propriedade de valor MVszW definida como uma matriz de cadeias de caracteres Unicode terminadas por caractere nulo. Para obter mais informações, [consulte o tópico SWStringArray.](swstringarray.md) 
    
> [!NOTE]
> O SPropValue é armazenado em uma propriedade MAPI no intervalo interno do PST. Essa propriedade está inacessível para aplicativos MAPI comuns. 
  
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada de função foi bem-sucedida.
    
## <a name="remarks"></a>Comentários

Registros persistentes podem afetar adversamente o desempenho de aplicativos, como o Outlook e o Windows Desktop Search, que abrem PSTs. Considere o efeito de desempenho ao usar ou expandir o uso de registros persistentes.
  
> [!IMPORTANT]
> Esse método é implementado somente para Unicode. Além disso, ele falhará preventivamente se qualquer um dos caminhos na matriz não tiver uma extensão de nome de arquivo .dll. 
  
## <a name="see-also"></a>Confira também

- [IPSTOVERRIDE1 : IUnknown](ipstoverride1iunknown.md) 
- [IPSTOVERRIDEREQ : IUnknown](ipstoverridereqiunknown.md)

