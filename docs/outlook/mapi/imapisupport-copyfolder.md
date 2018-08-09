---
title: IMAPISupportCopyFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.CopyFolder
api_type:
- COM
ms.assetid: c2e0939f-0668-473f-856c-a27af094070b
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 0b079b311a68459a43b0a7659ddfbe94d96d7f9c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767213"
---
# <a name="imapisupportcopyfolder"></a>IMAPISupport::CopyFolder

  
  
**Aplica-se a**: Outlook 
  
Copia ou move uma pasta da pasta pai atual para outra pasta pai.
  
```cpp
HRESULT CopyFolder(
  LPCIID lpSrcInterface,
  LPVOID lpSrcFolder,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  LPVOID lpDestFolder,
  LPSTR lpszNewFolderName,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parâmetros

 _lpSrcInterface_
  
> [in] Um ponteiro para o identificador de interface (IID) que representa a interface para ser usado para acessar a pasta pai da pasta a ser copiado ou movido.
    
 _lpSrcFolder_
  
> [in] Um ponteiro para a pasta pai da pasta a ser copiado ou movido. 
    
 _cbEntryID_
  
> [in] A contagem de bytes no identificador de entrada apontado pela _lpEntryID_.
    
 _lpEntryID_
  
> [in] Um ponteiro para o identificador de entrada da pasta a ser copiado ou movido. 
    
 _lpInterface_
  
> [in] Reservado; deve ser NULL.
    
 _lpDestFolder_
  
> [in] Um ponteiro para a pasta que está para receber a pasta a ser copiado ou movido.
    
 _lpszNewFolderName_
  
> [in] Um ponteiro para o nome da pasta movido ou copiada; Caso contrário, NULL, que indica que a pasta movida ou copiada deve ter o mesmo nome como a pasta de origem (a pasta indicada por _lpEntryID_).
    
 _ulUIParam_
  
> [in] Uma alça da janela para a caixa de diálogo de indicador de progresso e windows relacionado. O parâmetro _ulUIParam_ é ignorado, a menos que o sinalizador FOLDER_DIALOG é definido no parâmetro _ulFlags_ . 
    
 _lpProgress_
  
> [in] Um ponteiro para um objeto de progresso que exibe um indicador de progresso. Se NULL for passado _lpProgress_, o provedor de armazenamento de mensagem exibe um indicador de progresso usando a implementação de objeto de progresso MAPI. O parâmetro _lpProgress_ é ignorado, a menos que o sinalizador FOLDER_DIALOG está definido na _ulFlags_.
    
 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla como a operação de cópia ou movimentação é realizada. Sinalizadores a seguir podem ser definidos:
    
COPY_SUBFOLDERS 
  
> Todas as subpastas da pasta devem ser copiadas ou movidas. Quando COPY_SUBFOLDERS não estiver definida para uma operação de cópia, somente a pasta identificada pelo _lpEntryID_ é copiada. Com uma operação de movimentação, o comportamento COPY_SUBFOLDERS é o padrão independentemente se o sinalizador está definido. 
    
FOLDER_DIALOG 
  
> Solicita a exibição de um indicador de progresso.
    
FOLDER_MOVE 
  
> A pasta deve ser movida, em vez de copiados. Se FOLDER_MOVE não estiver definida, a pasta será copiada.
    
MAPI_UNICODE 
  
> O nome da pasta é no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, o nome da pasta é no formato ANSI.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A pasta foi copiada ou movida com êxito.
    
MAPI_E_COLLISION 
  
> O nome da pasta que está sendo movido ou copiadas é igual de uma subpasta na pasta de destino. O provedor de armazenamento de mensagem requer que os nomes de pasta ser exclusivos. A operação interrompe sem concluir.
    
MAPI_W_PARTIAL_COMPLETION 
  
> A chamada foi bem-sucedida, mas nem todas as entradas foram copiadas com êxito. Quando esse aviso é retornado, a chamada deve ser manipulada com êxito. Para testar esse aviso, use a macro **HR_FAILED** . Para obter mais informações, consulte [Usando Macros para tratamento de erros](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Comentários

O método **IMAPISupport::CopyFolder** é implementado para objetos de suporte do provedor de repositório de mensagem. Provedores de armazenamento de mensagens podem chamar **IMAPISupport::CopyFolder** na sua implementação do [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md) para copiar ou mover uma única pasta da pasta pai de um para outro. 
  
 **IMAPISupport::CopyFolder** adiciona a pasta movida ou copiada como uma subpasta da pasta de destino. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

 **IMAPISupport::CopyFolder** permite simultâneo de renomear e mover de pastas e as cópias ou movimentações de subpastas da pasta afetada. Para copiar ou mover todas as subpastas aninhadas na pasta copiada ou movida, passe o sinalizador COPY_SUBFOLDERS em _ulFlags_. 
  
Espera que a seguir retorna valores sob as seguintes condições:
  
|**Condição**|**Valor retornado**|
|:-----|:-----|
|**CopyFolder** com êxito copiado ou movido a pasta e todas as suas subpastas, se aplicável.  <br/> |S_OK  <br/> |
|**CopyFolder** foi capaz de copiar ou mover todas as pastas com êxito.  <br/> |MAPI_W_PARTIAL_COMPLETION  <br/> |
|**CopyFolder** não pôde concluir.  <br/> |Qualquer valor de erro  <br/> |
   
Se **CopyFolder** retornará um valor de erro, não continue na pressuposição de que nenhum trabalho foi executado. Uma ou mais pastas poderiam ter foi copiadas ou movidas antes de **CopyFolder** apresentaram falha. 
  
## <a name="see-also"></a>Confira também



[IMAPISupport: IUnknown](imapisupportiunknown.md)

