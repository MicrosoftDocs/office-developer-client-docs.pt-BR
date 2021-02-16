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
ms.openlocfilehash: 734e53c1e897c902c72319aa6f2d3d7af2d23fb6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431705"
---
# <a name="imsprovidercomparestoreids"></a>IMSProvider::CompareStoreIDs

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Compara dois identificadores de entrada do armazenamento de mensagens para determinar se eles se referem ao mesmo objeto de armazenamento.
  
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
  
> [in] O tamanho, em bytes, do identificador de entrada apontado pelo parâmetro  _lpEntryID1_  _._
    
 _lpEntryID1_
  
> [in] Um ponteiro para o identificador da primeira entrada a ser comparado.
    
 _cbEntryID2_
  
> [in] O tamanho, em bytes, do identificador de entrada apontado pelo parâmetro  _lpEntryID2_  _._
    
 _lpEntryID2_
  
> [in] Um ponteiro para o segundo identificador de entrada a ser comparado.
    
 _ulFlags_
  
> [in] Reservado; deve ser zero.
    
 _lpulResult_
  
> [out] Um ponteiro para o resultado retornado da comparação. TRUE se os dois identificadores de entrada se referirem ao mesmo objeto; caso contrário, FALSE.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor ou os valores esperados.
    
## <a name="remarks"></a>Comentários

O MAPI chama o método **IMSProvider::CompareStoreIDs** quando ele processa uma chamada para o método [IMAPISession::OpenMsgStore.](imapisession-openmsgstore.md) **CompareStoreIDs** é chamado neste ponto para determinar qual seção de perfil, se alguma, está associada ao repositório de mensagens que está sendo aberto. Uma **chamada CompareStoreIDs** pode ser feita quando nenhum repositório de mensagens está aberto para um provedor de repositório específico. Além disso, o MAPI também chama **CompareStoreIDs** quando processa uma chamada de provedor de repositório para o método [IMAPISupport::OpenProfileSection.](imapisupport-openprofilesection.md) 
  
Os identificadores de entrada comparados por **CompareStoreIDs** são ambos para a biblioteca de vínculo dinâmico (DLL) do provedor de repositório atual e são identificadores de entrada de repositório não mapeados. Para obter mais informações sobre identificadores de entrada do repositório de quebra, consulte [IMAPISupport::WrapStoreEntryID](imapisupport-wrapstoreentryid.md).
  
Comparar identificadores de entrada é útil porque um objeto pode ter mais de um identificador de entrada válido. Isso pode ocorrer, por exemplo, depois que uma nova versão de um provedor de armazenamento de mensagens é instalada. 
  
## <a name="see-also"></a>Confira também



[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)
  
[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)
  
[IMAPISupport::WrapStoreEntryID](imapisupport-wrapstoreentryid.md)
  
[IMSProvider : IUnknown](imsprovideriunknown.md)

