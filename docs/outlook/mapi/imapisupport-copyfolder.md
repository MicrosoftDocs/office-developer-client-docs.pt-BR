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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341024"
---
# <a name="imapisupportcopyfolder"></a>IMAPISupport::CopyFolder

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
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
  
> no Um ponteiro para o identificador de interface (IID) que representa a interface a ser usada para acessar a pasta pai da pasta a ser copiada ou movida.
    
 _lpSrcFolder_
  
> no Um ponteiro para a pasta pai da pasta a ser copiada ou movida. 
    
 _cbEntryID_
  
> no A contagem de bytes no identificador de entrada apontado por _lpEntryID_.
    
 _lpEntryID_
  
> no Um ponteiro para o identificador de entrada da pasta a ser copiado ou movido. 
    
 _lpInterface_
  
> no Serve deve ser nulo.
    
 _lpDestFolder_
  
> no Um ponteiro para a pasta que receberá a pasta a ser copiada ou movida.
    
 _lpszNewFolderName_
  
> no Um ponteiro para o nome da pasta copiada ou movida; caso contrário, NULL, que indica que a pasta copiada ou movida deverá ter o mesmo nome da pasta de origem (a pasta apontada por _lpEntryID_).
    
 _ulUIParam_
  
> no Uma alça da janela da caixa de diálogo indicador de progresso e janelas relacionadas. O parâmetro _ulUIParam_ é ignorado, a menos que o sinalizador FOLDER_DIALOG esteja definido no parâmetro _parâmetroulflags_ . 
    
 _lpProgress_
  
> no Um ponteiro para um objeto Progress que exibe um indicador de progresso. Se NULL for passado no _lpProgress_, o provedor de armazenamento de mensagens exibirá um indicador de progresso usando a implementação do objeto de progresso MAPI. O parâmetro _lpProgress_ é ignorado, a menos que o sinalizador FOLDER_DIALOG esteja definido em _parâmetroulflags_.
    
 _ulFlags_
  
> no Uma bitmask de sinalizadores que controlam como a operação de cópia ou movimentação é realizada. Os seguintes sinalizadores podem ser definidos:
    
COPY_SUBFOLDERS 
  
> Todas as subpastas da pasta devem ser copiadas ou movidas. Quando o COPY_SUBFOLDERS não está definido para uma operação de cópia, somente a pasta identificada por _lpEntryID_ é copiada. Com uma operação de movimentação, o comportamento COPY_SUBFOLDERS é o padrão, independentemente de o sinalizador ser definido. 
    
FOLDER_DIALOG 
  
> Solicita a exibição de um indicador de progresso.
    
FOLDER_MOVE 
  
> A pasta deve ser movida ao invés de ser copiada. Se FOLDER_MOVE não for definido, a pasta será copiada.
    
MAPI_UNICODE 
  
> O nome da pasta está no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, o nome da pasta estará no formato ANSI.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A pasta foi copiada ou movida com êxito.
    
MAPI_E_COLLISION 
  
> O nome da pasta que está sendo movida ou copiada é o mesmo que o de uma subpasta na pasta de destino. O provedor de repositório de mensagens exige que os nomes das pastas sejam exclusivos. A operação é interrompida sem conclusão.
    
MAPI_W_PARTIAL_COMPLETION 
  
> A chamada teve êxito, mas nem todas as entradas foram copiadas com êxito. Quando esse aviso é retornado, a chamada deve ser tratada como bem-sucedida. Para testar esse aviso, use a macro **HR_FAILED** . Para obter mais informações, consulte [usando macros para tratamento de erros](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Comentários

O método **IMAPISupport:: CopyFolder** é implementado para objetos de suporte do provedor de repositório de mensagens. Os provedores de repositório de mensagens podem chamar **IMAPISupport:: CopyFolder** em sua implementação de [IMAPIFolder:: CopyFolder](imapifolder-copyfolder.md) para copiar ou mover uma única pasta de uma pasta pai para outra. 
  
 **IMAPISupport:: CopyFolder** adiciona a pasta copiada ou movida como uma subpasta da pasta de destino. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

 **IMAPISupport:: CopyFolder** permite renomear e mover simultaneamente pastas e a cópia ou movimentação de subpastas da pasta afetada. Para copiar ou mover todas as subpastas aninhadas na pasta copiada ou movida, passe o sinalizador COPY_SUBFOLDERS no _parâmetroulflags_. 
  
Espere os seguintes valores de retorno sob as seguintes condições:
  
|**Condition**|**Valor retornado**|
|:-----|:-----|
|**CopyFolder** copiou ou moveu com êxito a pasta e todas as suas subpastas, se aplicável.  <br/> |S_OK  <br/> |
|O **CopyFolder** não pôde copiar ou mover com êxito todas as pastas.  <br/> |MAPI_W_PARTIAL_COMPLETION  <br/> |
|**CopyFolder** não pôde ser concluída.  <br/> |Qualquer valor de erro  <br/> |
   
Se **CopyFolder** retornar um valor de erro, não prossiga com a suposição de que nenhum trabalho foi realizado. Uma ou mais pastas podem ter sido copiadas ou movidas antes do **CopyFolder** ter falhado. 
  
## <a name="see-also"></a>Confira também



[IMAPISupport: IUnknown](imapisupportiunknown.md)

