---
title: IMSProviderCompareStoreIDs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSProvider.CompareStoreIDs
api_type:
- COM
ms.assetid: c3e3cfaa-9c4a-482a-9411-9c4ab01d312f
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 57b8438d655b3bc5b708fd7ed6734554a3a23ac4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585987"
---
# <a name="imsprovidercomparestoreids"></a>IMSProvider::CompareStoreIDs

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Compara dois mensagem repositório identificadores de entrada para determinar se eles se referem ao mesmo objeto store.
  
```cpp
HRESULT CompareStoreIDs(
  ULONG cbEntryID1,
  LPENTRYID lpEntryID1,
  ULONG cbEntryID2,
  LPENTRYID lpEntryID2,
  ULONG ulFlags,
  ULONG FAR * lpulResult
);
```

## <a name="parameters"></a>Parâmetros

 _cbEntryID1_
  
> [in] O tamanho, em bytes, do identificador de entrada apontado pelo parâmetro _lpEntryID1_ _._
    
 _lpEntryID1_
  
> [in] Um ponteiro para o primeiro identificador de entrada a ser comparada.
    
 _cbEntryID2_
  
> [in] O tamanho, em bytes, do identificador de entrada apontado pelo parâmetro _lpEntryID2_ _._
    
 _lpEntryID2_
  
> [in] Um ponteiro para o segundo identificador de entrada a ser comparada.
    
 _ulFlags_
  
> [in] Reservado; deve ser zero.
    
 _lpulResult_
  
> [out] Um ponteiro para o resultado da comparação. TRUE se os identificadores de dois entrada se referir ao mesmo objeto; Caso contrário, FALSE.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
## <a name="remarks"></a>Comentários

MAPI chama o método **IMSProvider::CompareStoreIDs** quando ele processa uma chamada ao método [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) . **CompareStoreIDs** é chamado, nesse momento, para determinar qual seção de perfil, se houver, está associada com o armazenamento de mensagens está sendo aberto. Uma chamada de **CompareStoreIDs** pode ser feita quando nenhum armazenamentos de mensagem estão abertos para um provedor de armazenamento específica. Além disso, o MAPI também chama **CompareStoreIDs** quando ele processa uma chamada do provedor de repositório para o método [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) . 
  
Os identificadores de entrada comparados por **CompareStoreIDs** são ambos para as atuais armazenam biblioteca do provedor de vínculo dinâmico (DLL) e são os dois identificadores de entrada do repositório desfeita. Para obter mais informações sobre identificadores de entrada do repositório de disposição, consulte [IMAPISupport::WrapStoreEntryID](imapisupport-wrapstoreentryid.md).
  
Comparar os identificadores de entrada é útil porque um objeto pode ter mais de um identificador de entrada válida. Isso pode ocorrer, por exemplo, depois que uma nova versão de um provedor de armazenamento de mensagens é instalada. 
  
## <a name="see-also"></a>Confira também



[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)
  
[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)
  
[IMAPISupport::WrapStoreEntryID](imapisupport-wrapstoreentryid.md)
  
[IMSProvider : IUnknown](imsprovideriunknown.md)

