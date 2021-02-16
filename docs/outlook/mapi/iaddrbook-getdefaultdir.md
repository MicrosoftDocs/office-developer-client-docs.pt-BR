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
ms.openlocfilehash: d9ad74d8ae02a49ee3c222394caedfd571f84b1c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436871"
---
# <a name="iaddrbookgetdefaultdir"></a>IAddrBook::GetDefaultDir

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Retorna o identificador de entrada para o contêiner inicial do address book.
  
```cpp
HRESULT GetDefaultDir(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a>Parâmetros

 _lpcbEntryID_
  
> [out] Um ponteiro para a contagem de byte no identificador de entrada apontado pelo _parâmetro lppEntryID._ 
    
 _lppEntryID_
  
> [out] Um ponteiro para um ponteiro para o identificador de entrada do contêiner padrão.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O identificador de entrada do contêiner padrão foi retornado com êxito.
    
## <a name="remarks"></a>Comentários

Os aplicativos cliente e provedores de serviços chamam o **método GetDefaultDir** para recuperar o identificador de entrada do contêiner de agendamento de endereços padrão. O contêiner padrão é o que o usuário vê exibido no livro de endereços quando o livro de endereços é aberto pela primeira vez. Se um contêiner padrão não tiver sido definido por uma chamada para o método [IAddrBook::SetDefaultDir,](iaddrbook-setdefaultdir.md) o MAPI atribuirá como contêiner padrão o primeiro contêiner com nomes que não são o pab (lista de endereços pessoal). Se esse contêiner não for encontrado, o PAB se tornará o contêiner padrão. 
  
Para definir o diretório padrão, um cliente ou provedor chama o **método SetDefaultDir.** Os clientes e provedores não têm que chamar o [método IMAPIProp::SaveChanges;](imapiprop-savechanges.md) como as alterações no livro de endereços não são transacionados, as alterações são permanentes imediatamente. 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnOpenDefaultDir  <br/> |MFCMAPI usa o **método GetDefaultDir** para obter a ID do contêiner de livro de endereços padrão.  <br/> |
   
## <a name="see-also"></a>Confira também



[IAddrBook::SetDefaultDir](iaddrbook-setdefaultdir.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[Propriedade canônica PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

