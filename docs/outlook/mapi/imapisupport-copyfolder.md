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
ms.openlocfilehash: 11ee944a14f8c9bd881b9c79a4ce66817275e73a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420882"
---
# <a name="imapisupportcopyfolder"></a>IMAPISupport::CopyFolder

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Copia ou move uma pasta de sua pasta pai atual para outra pasta pai.
  
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
  
> [in] Um ponteiro para o IID (identificador de interface) que representa a interface a ser usada para acessar a pasta pai da pasta a ser copiada ou movida.
    
 _lpSrcFolder_
  
> [in] Um ponteiro para a pasta pai da pasta a ser copiada ou movida. 
    
 _cbEntryID_
  
> [in] A contagem de byte no identificador de entrada apontado por  _lpEntryID_.
    
 _lpEntryID_
  
> [in] Um ponteiro para o identificador de entrada da pasta a ser copiada ou movida. 
    
 _lpInterface_
  
> [in] Reservado; deve ser NULL.
    
 _lpDestFolder_
  
> [in] Um ponteiro para a pasta que deve receber a pasta a ser copiada ou movida.
    
 _lpszNewFolderName_
  
> [in] Um ponteiro para o nome da pasta copiada ou movida; caso contrário, NULL, que indica que a pasta copiada ou movida deve ter o mesmo nome da pasta de origem (a pasta apontada por  _lpEntryID_).
    
 _ulUIParam_
  
> [in] Um alça da janela para a caixa de diálogo do indicador de progresso e janelas relacionadas. O _parâmetro ulUIParam é_ ignorado, a menos que o FOLDER_DIALOG padrão seja definido no parâmetro _ulFlags._ 
    
 _lpProgress_
  
> [in] Um ponteiro para um objeto de progresso que exibe um indicador de progresso. Se NULL for passado  _em lpProgress_, o provedor de armazenamento de mensagens exibirá um indicador de progresso usando a implementação de objeto de progresso MAPI. O  _parâmetro lpProgress_ é ignorado, a menos que o sinalizador FOLDER_DIALOG seja definido em  _ulFlags_.
    
 _ulFlags_
  
> [in] Uma máscara de bits de sinalizadores que controla como a operação de cópia ou movimentação é realizada. Os sinalizadores a seguir podem ser definidos:
    
COPY_SUBFOLDERS 
  
> Todas as subpastas da pasta devem ser copiadas ou movidas. Quando COPY_SUBFOLDERS não estiver definida para uma operação de cópia, somente a pasta identificada por  _lpEntryID_ será copiada. Com uma operação de movimentação, o COPY_SUBFOLDERS padrão é o padrão, independentemente de o sinalizador ser definido. 
    
FOLDER_DIALOG 
  
> Solicita a exibição de um indicador de progresso.
    
FOLDER_MOVE 
  
> A pasta deve ser movida em vez de copiada. Se FOLDER_MOVE não estiver definida, a pasta será copiada.
    
MAPI_UNICODE 
  
> O nome da pasta está no formato Unicode. Se o MAPI_UNICODE sinalizador não estiver definido, o nome da pasta está no formato ANSI.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A pasta foi copiada ou movida com êxito.
    
MAPI_E_COLLISION 
  
> O nome da pasta que está sendo movida ou copiada é igual ao de uma subpasta na pasta de destino. O provedor de armazenamento de mensagens exige que os nomes das pastas sejam exclusivos. A operação é interrompida sem concluir.
    
MAPI_W_PARTIAL_COMPLETION 
  
> A chamada foi bem-sucedida, mas nem todas as entradas foram copiadas com êxito. Quando esse aviso é retornado, a chamada deve ser tratada como bem-sucedida. Para testar esse aviso, use a **HR_FAILED** macro. Para obter mais informações, consulte [Usando macros para tratamento de erros.](using-macros-for-error-handling.md)
    
## <a name="remarks"></a>Comentários

O **método IMAPISupport::CopyFolder** é implementado para objetos de suporte do provedor de armazenamento de mensagens. Os provedores de armazenamento de mensagens podem chamar **IMAPISupport::CopyFolder** na implementação de [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md) para copiar ou mover uma única pasta de uma pasta pai para outra. 
  
 **IMAPISupport::CopyFolder** adiciona a pasta copiada ou movida como uma subpasta da pasta de destino. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

 **IMAPISupport::CopyFolder** permite renomeação e movimentação simultâneas de pastas e a cópia ou movimentação de subpastas da pasta afetada. Para copiar ou mover todas as subpastas aninhadas na pasta copiada ou movida, passe o sinalizador COPY_SUBFOLDERS em  _ulFlags_. 
  
Espere os seguintes valores de retorno sob as seguintes condições:
  
|**Condition**|**Valor de retorno**|
|:-----|:-----|
|**CopyFolder** copiou ou moveu com êxito a pasta e todas as suas subpastas, se aplicável.  <br/> |S_OK  <br/> |
|**CopyFolder** não pôde copiar ou mover todas as pastas com êxito.  <br/> |MAPI_W_PARTIAL_COMPLETION  <br/> |
|**CopyFolder** não pôde ser concluída.  <br/> |Qualquer valor de erro  <br/> |
   
Se **CopyFolder** retornar um valor de erro, não prossiga com a suposição de que nenhum trabalho foi feito. Uma ou mais pastas podem ter sido copiadas ou movidas antes da falha do **CopyFolder.** 
  
## <a name="see-also"></a>Confira também



[IMAPISupport: IUnknown](imapisupportiunknown.md)

