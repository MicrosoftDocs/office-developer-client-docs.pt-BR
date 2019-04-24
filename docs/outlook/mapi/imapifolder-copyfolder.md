---
title: IMAPIFolderCopyFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.CopyFolder
api_type:
- COM
ms.assetid: 2c1c25c6-1aec-4d9e-a2a3-bf1b4a2908b8
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 3d9c1e88b12baf50593212a3ae3c02907ce6617b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280175"
---
# <a name="imapifoldercopyfolder"></a>IMAPIFolder::CopyFolder

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Copia ou move uma subpasta.
  
```cpp
HRESULT CopyFolder(
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

 _cbEntryID_
  
> no A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID_ . 
    
 _lpEntryID_
  
> no Um ponteiro para o identificador de entrada da subpasta a ser copiado ou movido.
    
 _lpInterface_
  
> no Um ponteiro para o identificador de interface (IID) que representa a interface a ser usada para acessar a pasta para a qual o parâmetro _lpDestFolder_ aponta. Passar NULL faz com que o provedor de serviços retorne a interface de pasta padrão, [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md). Os valores válidos para _lpInterface_ incluem IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer e IID_IMAPIFolder. 
    
 _lpDestFolder_
  
> no Um ponteiro para a pasta aberta para receber a subpasta copiada ou movida.
    
 _lpszNewFolderName_
  
> no Um ponteiro para o nome da pasta copiada ou movida em seu novo destino. Se _lpszNewFolderName_ estiver definido como nulo, o nome da subpasta de origem será usado para o nome da pasta de destino. 
    
 _ulUIParam_
  
> no Uma alça para a janela pai do indicador de progresso. O parâmetro _ulUIParam_ é ignorado, a menos que o sinalizador FOLDER_DIALOG no parâmetro _parâmetroulflags_ seja definido. 
    
 _lpProgress_
  
> no Um ponteiro para um objeto Progress que exibe um indicador de progresso. Se NULL for passado no _lpProgress_, o provedor de armazenamento de mensagens exibirá um indicador de progresso usando a implementação do objeto de progresso MAPI. O parâmetro _lpProgress_ é ignorado, a menos que o sinalizador FOLDER_DIALOG esteja definido em _parâmetroulflags_.
    
 _ulFlags_
  
> no Uma bitmask de sinalizadores que controlam a operação de cópia ou movimentação. Os seguintes sinalizadores podem ser definidos:
    
COPY_SUBFOLDERS 
  
> Todas as subpastas na subpasta a serem copiadas também devem ser copiadas. Quando COPY_SUBFOLDERS não é definido para uma operação de cópia, somente a subpasta identificada por _lpEntryID_ é copiada. Com uma operação de movimentação, o comportamento COPY_SUBFOLDERS é o padrão, independentemente de o sinalizador ser definido. 
    
FOLDER_DIALOG 
  
> Solicita a exibição de um indicador de progresso.
    
FOLDER_MOVE 
  
> A subpasta deve ser movida ao invés de ser copiada. Se FOLDER_MOVE não for definido, a subpasta será copiada.
    
MAPI_DECLINE_OK 
  
> Informa ao provedor de repositório de mensagens que se ele implementa **CopyFolder** chamando o IMAPISupport do seu objeto support [::D ocopyto](imapisupport-docopyto.md) ou [IMAPISupport::D método ocopyprops](imapisupport-docopyprops.md) , **CopyFolder** deve retornar imediatamente MAPI_E_ DECLINE_COPY. 
    
MAPI_UNICODE 
  
> O nome da pasta de destino está no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, o nome da pasta estará no formato ANSI.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A pasta especificada foi copiada ou movida com êxito.
    
MAPI_E_BAD_CHARWIDTH 
  
> O sinalizador MAPI_UNICODE foi definido e o provedor do repositório de mensagens não tem suporte para Unicode ou o MAPI_UNICODE não foi definido e o provedor de repositório de mensagens oferece suporte somente a Unicode.
    
MAPI_E_COLLISION 
  
> O nome da pasta que está sendo movida ou copiada é o mesmo que o de uma subpasta na pasta de destino. O provedor de repositório de mensagens requer nomes de pastas exclusivos.
    
MAPI_E_DECLINE_COPY 
  
> O provedor implementa esse método chamando um método de objeto support e o chamador passou o sinalizador MAPI_DECLINE_OK.
    
MAPI_E_FOLDER_CYCLE 
  
> A pasta de origem direta ou indiretamente contém a pasta de destino. Um trabalho significativo pode ter sido realizado antes que essa condição fosse descoberta, portanto, a pasta de origem e destino pode ser parcialmente modificada. 
    
MAPI_W_PARTIAL_COMPLETION 
  
> A chamada teve êxito, mas nem todas as entradas foram copiadas com êxito. Quando esse aviso é retornado, a chamada deve ser tratada como bem-sucedida. Para testar esse aviso, use a macro **HR_FAILED** . Para obter mais informações, consulte [usando macros para tratamento de erros](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Comentários

O método **IMAPIFolder:: CopyFolder** copia ou move uma subpasta de um local para outro. A subpasta que está sendo copiada ou movida é adicionada à pasta de destino como uma subpasta. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Quando a operação de copiar ou mover envolve mais de uma pasta, conforme indicado pela definição do sinalizador COPY_SUBFOLDERS, execute a operação o mais completo possível para cada pasta. Às vezes, uma das pastas a serem movidas ou copiadas não existe ou já foi movida ou copiada em outro lugar. Não pare a operação prematuramente, a menos que ocorra uma falha que esteja além do seu controle, como a falta de memória, ficando sem espaço em disco ou corrupção no repositório de mensagens.
  
Tente reter todos os identificadores de entrada de mensagem nas mensagens copiadas. Você também deve tentar preservar os identificadores de entrada, mas isso não é necessário. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Espere estes valores de retorno sob as condições a seguir.
  
|**Condition**|**Valor retornado**|
|:-----|:-----|
|**CopyFolder** copiou ou moveu com êxito todas as mensagens e subpastas.  <br/> |S_OK  <br/> |
|O **CopyFolder** não pôde copiar ou mover com êxito todas as mensagens e subpastas.  <br/> |MAPI_W_PARTIAL_COMPLETION ou MAPI_E_NOT_FOUND  <br/> |
|**CopyFolder** não pôde ser concluída.  <br/> |Qualquer valor de erro, exceto MAPI_E_NOT_FOUND  <br/> |
   
Quando o **CopyFolder** não puder ser concluído, não presuma que nenhum trabalho foi realizado. O **CopyFolder** pode ter sido capaz de copiar ou mover uma ou mais mensagens e subpastas antes de encontrar o erro. 
  
Se um identificador de entrada para uma pasta que não existe é passado no _lpEntryID_, **CopyFolder** retorna MAPI_W_PARTIAL_COMPLETION ou MAPI_E_NOT_FOUND, dependendo da implementação do repositório de mensagens. 
  
Dependendo do provedor de repositório de mensagens, o identificador de entrada da mensagem original pode ou não ser preservado na mensagem copiada. Você deve preservar os identificadores de entrada sempre que possível, mas não é um requisito. Em geral, você pode depender dos seguintes cenários:
  
- Quando você move uma pasta entre dois tipos diferentes de repositórios de mensagens, o identificador de entrada é garantido para alteração.
    
- Quando você move uma pasta entre dois repositórios de mensagens do mesmo tipo, o identificador de entrada quase sempre é alterado.
    
- Quando você move uma pasta para outro local no mesmo repositório de mensagens, o identificador de entrada pode ou não ser alterado, dependendo do provedor de armazenamento de mensagens.
    
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MsgStoreDlg. cpp  <br/> |CMsgStoreDlg:: OnPasteFolder  <br/> |MFCMAPI usa o método **IMAPIFolder:: CopyFolder** para copiar pastas de um local para outro. MFCMAPI memoriza a pasta de origem durante a operação de cópia e, na verdade, realiza a cópia durante a operação de colagem.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

