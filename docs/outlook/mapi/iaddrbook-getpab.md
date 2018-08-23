---
title: IAddrBookGetPAB
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.GetPAB
api_type:
- COM
ms.assetid: 9830e09c-700f-469b-a54d-4e4e0583aa84
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 1f93ee653c9365488432c4e797b171a199c30107
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583712"
---
# <a name="iaddrbookgetpab"></a>IAddrBook::GetPAB

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Retorna o identificador de entrada do contêiner que é designado como o catálogo de endereços pessoal (PAB).
  
```cpp
HRESULT GetPAB(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a>Parâmetros

 _lpcbEntryID_
  
> [out] Um ponteiro para a contagem de bytes no identificador de entrada apontado pelo parâmetro _lppEntryID_ . 
    
 _lppEntryID_
  
> [out] Um ponteiro para um ponteiro para o identificador de entrada do PAB. O parâmetro _lppEntryID_ contém zero se nenhum contêiner foi designada como o PAB. 
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> O identificador de entrada do PAB foi retornado com êxito.
    
## <a name="remarks"></a>Comentários

Clientes chamar o método **GetPAB** para recuperar o identificador de entrada do contêiner designado como o PAB. Se um PAB não tiver sido estabelecido no perfil, MAPI selecionará como o PAB o primeiro contêiner na hierarquia de catálogo de endereços que permite modificações. 
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnOpenPAB  <br/> |MFCMAPI usa o método **GetPAB** para obter a ID do catálogo de endereços pessoal do usuário.  <br/> |
   
## <a name="see-also"></a>Confira também



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[Propriedade canônica PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

