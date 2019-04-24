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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317266"
---
# <a name="imsprovidercomparestoreids"></a>IMSProvider::CompareStoreIDs

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Compara dois identificadores de entrada de repositório de mensagens para determinar se eles se referem ao mesmo objeto Store.
  
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
  
> no O tamanho, em bytes, do identificador de entrada apontado pelo parâmetro _lpEntryID1_ _._
    
 _lpEntryID1_
  
> no Um ponteiro para o primeiro identificador de entrada a ser comparado.
    
 _cbEntryID2_
  
> no O tamanho, em bytes, do identificador de entrada apontado pelo parâmetro _lpEntryID2_ _._
    
 _lpEntryID2_
  
> no Um ponteiro para o segundo identificador de entrada ser comparado.
    
 _ulFlags_
  
> no Serve deve ser zero.
    
 _lpulResult_
  
> bota Um ponteiro para o resultado retornado da comparação. TRUE se os dois identificadores de entrada se referem ao mesmo objeto; caso contrário, FALSE.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada teve êxito e retornou o valor ou valores esperados.
    
## <a name="remarks"></a>Comentários

MAPI chama o método **IMSProvider:: CompareStoreIDs** quando processa uma chamada para o método [IMAPISession:: OpenMsgStore](imapisession-openmsgstore.md) . **CompareStoreIDs** é chamado neste ponto para determinar qual seção de perfil, se houver, está associada ao armazenamento de mensagens que está sendo aberto. Uma chamada **CompareStoreIDs** pode ser feita quando não há repositórios de mensagens abertos para um provedor de repositório específico. Além disso, o MAPI também chama **CompareStoreIDs** quando processa uma chamada do provedor de repositório para o método [IMAPISupport:: OpenProfileSection](imapisupport-openprofilesection.md) . 
  
Os identificadores de entrada comparados por **CompareStoreIDs** são para a biblioteca de vínculo dinâmico (DLL) do provedor de repositório atual e são identificadores de entrada de repositório não encapsulados. Para obter mais informações sobre identificadores de entrada de repositório de enrolamento, consulte [IMAPISupport:: WrapStoreEntryID](imapisupport-wrapstoreentryid.md).
  
A comparação de identificadores de entrada é útil porque um objeto pode ter mais de um identificador de entrada válido. Isso pode ocorrer, por exemplo, após a instalação de uma nova versão de um provedor de repositório de mensagens. 
  
## <a name="see-also"></a>Confira também



[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)
  
[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)
  
[IMAPISupport::WrapStoreEntryID](imapisupport-wrapstoreentryid.md)
  
[IMSProvider : IUnknown](imsprovideriunknown.md)

