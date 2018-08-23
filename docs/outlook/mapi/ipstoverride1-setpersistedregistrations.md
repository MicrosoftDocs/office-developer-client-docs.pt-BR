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
description: 'Modificado pela última vez: 08 de novembro de 2011'
ms.openlocfilehash: 3592584a08bf14725c0289831740e91fb8f1a5b2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587617"
---
# <a name="ipstoverride1setpersistedregistrations"></a>IPSTOVERRIDE1::SetPersistedRegistrations

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Registra os arquivos de pastas particulares (. pst) para desbloqueio automático, evitando mais chamadas para o HrTrustedPSTOverrideHandlerCallback.
  
```cpp
HRESULT SetPersistedRegistrations(
  SPropValue *pmval
);
```

## <a name="parameters"></a>Parâmetros

_pmval_
  
> [in] Uma estrutura de [SPropValue](spropvalue.md) que contém um ponteiro para o caminho da biblioteca de vínculo dinâmico (DLL) para registrar. A estrutura tem as seguintes características: 
    
   - Um ulPropTag de [PROP_TAG](prop_tag.md)(PT_MV_UNICODE, PROP_ID_NULL).
    
   - Uma propriedade de valor de MVszW é definida como uma matriz de cadeias de caracteres Unicode terminada em nulo. Para obter mais informações, consulte o tópico de [SWStringArray](swstringarray.md) . 
    
> [!NOTE]
> O SPropValue é armazenado em uma propriedade MAPI no intervalo de interno do PST. Essa propriedade está inacessível aos aplicativos comuns de MAPI. 
  
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada de função foi bem-sucedida.
    
## <a name="remarks"></a>Comentários

Os registros persistentes podem afetar negativamente o desempenho de aplicativos, como o Outlook e Windows Desktop Search, que PSTs ser aberto. Considere o efeito no desempenho ao usar ou expandindo o uso dos registros persistentes.
  
> [!IMPORTANT]
> Esse método é implementado apenas para Unicode. Além disso, ele preventivamente falhará se qualquer um dos caminhos na matriz não têm uma extensão de nome de arquivo de. dll. 
  
## <a name="see-also"></a>Confira também

- [IPSTOVERRIDE1 : IUnknown](ipstoverride1iunknown.md) 
- [IPSTOVERRIDEREQ : IUnknown](ipstoverridereqiunknown.md)

