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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 7309f65965fe3c88f927eeba0bbcccff97c479af
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766875"
---
# <a name="iaddrbookgetdefaultdir"></a>IAddrBook::GetDefaultDir

  
  
**Aplica-se a**: Outlook 
  
Retorna o identificador de entrada para o contêiner de catálogo de endereços inicial.
  
```cpp
HRESULT GetDefaultDir(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a>Par�metros

 _lpcbEntryID_
  
> [out] Um ponteiro para a contagem de bytes no identificador de entrada apontado pelo parâmetro _lppEntryID_ . 
    
 _lppEntryID_
  
> [out] Um ponteiro para um ponteiro para o identificador de entrada do contêiner padrão.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> O identificador de entrada do contêiner padrão era retornado com êxito.
    
## <a name="remarks"></a>Coment�rios

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
  
[Propriedade canônico de PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)
  
[IAddrBook: IMAPIProp](iaddrbookimapiprop.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

