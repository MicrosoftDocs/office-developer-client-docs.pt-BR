---
title: IAddrBookGetDefaultDir
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.GetDefaultDir
api_type:
- COM
ms.assetid: 7a9fdf3f-fd76-40fb-8217-967c6efba5f6
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: a9f0fac76f06bd638aeff89ff096507209cc0287
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568452"
---
# <a name="iaddrbookgetdefaultdir"></a>IAddrBook::GetDefaultDir

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Retorna o identificador de entrada para o contêiner de catálogo de endereços inicial.
  
```cpp
HRESULT GetDefaultDir(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a>Parâmetros

 _lpcbEntryID_
  
> [out] Um ponteiro para a contagem de bytes no identificador de entrada apontado pelo parâmetro _lppEntryID_ . 
    
 _lppEntryID_
  
> [out] Um ponteiro para um ponteiro para o identificador de entrada do contêiner padrão.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> O identificador de entrada do contêiner padrão era retornado com êxito.
    
## <a name="remarks"></a>Comentários

Provedores de serviços e aplicativos cliente chamar o método **GetDefaultDir** para recuperar o identificador de entrada do contêiner de catálogo de endereços padrão. O contêiner padrão é o que o usuário vê exibido no catálogo de endereços quando o catálogo de endereços é aberto pela primeira vez. Se um recipiente padrão não tiver sido definido por uma chamada para o método [IAddrBook::SetDefaultDir](iaddrbook-setdefaultdir.md) , MAPI atribui como o contêiner padrão o primeiro recipiente com nomes que não seja o catálogo de endereços pessoal (PAB). Se tais um contêiner não for encontrado, o PAB torna-se o contêiner padrão. 
  
Para definir o padrão de diretório, um cliente ou o provedor chama o método de **SetDefaultDir** . Clientes e provedores não precisará chamar o método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) ; porque as alterações ao catálogo de endereços não serão transacionadas, alterações são feitas imediatamente permanentes. 
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnOpenDefaultDir  <br/> |MFCMAPI usa o método **GetDefaultDir** para obter a ID para o contêiner de catálogo de endereços padrão.  <br/> |
   
## <a name="see-also"></a>Confira também



[IAddrBook::SetDefaultDir](iaddrbook-setdefaultdir.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[Propriedade canônica PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

