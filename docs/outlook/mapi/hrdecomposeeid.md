---
title: HrDecomposeEID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrDecomposeEID
api_type:
- COM
ms.assetid: 4847838a-2ad8-4927-8f78-7fa5c8eb54eb
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: e66d48b6caefe0fee67f41ea829db3201751cf27
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766783"
---
# <a name="hrdecomposeeid"></a>HrDecomposeEID

  
  
**Aplica-se a**: Outlook 
  
Separa o identificador de entrada compostos de um objeto, geralmente em uma mensagem em um armazenamento de mensagens, no identificador de entrada desse objeto no repositório e o identificador de entrada da loja.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Aplicativos cliente  <br/> |
   
```cpp
HrDecomposeEID(
  LPMAPISESSION psession,
  ULONG cbEID,
  LPENTRYID pEID,
  ULONG FAR * pcbStoreEID,
  LPENTRYID FAR * ppStoreEID,
  ULONG FAR * pcbMsgEID,
  LPENTRYID FAR * ppMsgEID
);
```

## <a name="parameters"></a>Parâmetros

 _psession_
  
> [in] Ponteiro para a sessão em uso pelo aplicativo cliente. 
    
 _cbEID_
  
> [in] Tamanho, em bytes, do identificador de entrada compostos sejam separados. 
    
 _pEID_
  
> [in] Ponteiro para o identificador de entrada compostos sejam separados. 
    
 _pcbStoreEID_
  
> [out] Ponteiro para o tamanho retornado, em bytes, do identificador de entrada do repositório de mensagem que contém o objeto. Se o parâmetro _pEID_ aponta para um identificador de entrada noncompound, em seguida, o parâmetro _pcbStoreEID_ aponta para um valor de zero. 
    
 _ppStoreEID_
  
> [out] Ponteiro para um ponteiro para o identificador retornado de entrada do repositório de mensagem que contém o objeto. Se o parâmetro _pEID_ aponta para um identificador de entrada noncompound, NULL é retornado no parâmetro _ppStoreEID_ . 
    
 _pcbMsgEID_
  
> [out] Ponteiro para o tamanho retornado, em bytes, do identificador de entrada do objeto. Se o parâmetro _pEID_ aponta para um identificador de entrada noncompound, o parâmetro _pcbMsgEID_ é igual ao valor do parâmetro _cbEID_ . 
    
 _ppMsgEID_
  
> [out] Ponteiro para um ponteiro para o identificador de entrada retornados do objeto. Se o parâmetro _pEID_ aponta para um identificador de entrada noncompound, _ppMsgEID_ aponta para um ponteiro para uma cópia do identificador de entrada noncompound. 
    
## <a name="return-value"></a>Valor retornado

Nenhum.
  
## <a name="remarks"></a>Comentários

Se o identificador especificado pelo parâmetro _pEID_ for composto, ele é dividido no identificador de entrada do objeto dentro de seu armazenamento de mensagens e o identificador de entrada da loja. Cadeias de caracteres de identificador de entrada noncompound simplesmente são copiadas. O identificador composto sejam separados é geralmente uma criada pela função [HrComposeEID](hrcomposeeid.md) . 
  
## <a name="notes-to-callers"></a>Notas para chamadores

A memória que contém o parâmetro _pEID_ é liberada após a conclusão bem-sucedida dessa função. A implementação de chamada é responsável por liberar memória para os parâmetros de saída. 
  

