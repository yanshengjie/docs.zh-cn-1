---
title: "COR_FIELD_OFFSET 结构"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: COR_FIELD_OFFSET
api_location: mscoree.dll
api_type: COM
f1_keywords: COR_FIELD_OFFSET
helpviewer_keywords: COR_FIELD_OFFSET structure [.NET Framework metadata]
ms.assetid: cced5298-277f-4a5a-8ecf-a0050c1096ea
topic_type: apiref
caps.latest.revision: "9"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 8e821a9d4ffa5054f687eff7360bc8d7cefb9f09
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/21/2017
---
# <a name="corfieldoffset-structure"></a><span data-ttu-id="7a319-102">COR_FIELD_OFFSET 结构</span><span class="sxs-lookup"><span data-stu-id="7a319-102">COR_FIELD_OFFSET Structure</span></span>
<span data-ttu-id="7a319-103">存储一个类中的指定字段的偏移量。</span><span class="sxs-lookup"><span data-stu-id="7a319-103">Stores the offset, within a class, of the specified field.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7a319-104">语法</span><span class="sxs-lookup"><span data-stu-id="7a319-104">Syntax</span></span>  
  
```  
typedef struct COR_FIELD_OFFSET {  
    mdFieldDef  ridOfField;  
    ULONG       ulOffset;  
} COR_FIELD_OFFSET;  
```  
  
## <a name="members"></a><span data-ttu-id="7a319-105">成员</span><span class="sxs-lookup"><span data-stu-id="7a319-105">Members</span></span>  
  
|<span data-ttu-id="7a319-106">成员</span><span class="sxs-lookup"><span data-stu-id="7a319-106">Member</span></span>|<span data-ttu-id="7a319-107">描述</span><span class="sxs-lookup"><span data-stu-id="7a319-107">Description</span></span>|  
|------------|-----------------|  
|`ridOfField`|<span data-ttu-id="7a319-108">`mdFieldDef`元数据标记表示的字段。</span><span class="sxs-lookup"><span data-stu-id="7a319-108">An `mdFieldDef` metadata token that represents the field.</span></span>|  
|`ulOffset`|<span data-ttu-id="7a319-109">在它的类情况下，字段的偏移量。</span><span class="sxs-lookup"><span data-stu-id="7a319-109">The field's offset within its class.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="7a319-110">备注</span><span class="sxs-lookup"><span data-stu-id="7a319-110">Remarks</span></span>  
 <span data-ttu-id="7a319-111">[Imetadataimport:: Getclasslayout](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-getclasslayout-method.md)和[imetadataemit:: Setclasslayout](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-setclasslayout-method.md)方法接受类型的参数`COR_FIELD_OFFSET`。</span><span class="sxs-lookup"><span data-stu-id="7a319-111">[IMetaDataImport::GetClassLayout](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-getclasslayout-method.md) and [IMetaDataEmit::SetClassLayout](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-setclasslayout-method.md) methods take a parameter of type `COR_FIELD_OFFSET`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7a319-112">要求</span><span class="sxs-lookup"><span data-stu-id="7a319-112">Requirements</span></span>  
 <span data-ttu-id="7a319-113">**平台：**请参阅[系统要求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="7a319-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7a319-114">**标头：** CorHdr.h、 CorProf.idl</span><span class="sxs-lookup"><span data-stu-id="7a319-114">**Header:** CorHdr.h, CorProf.idl</span></span>  
  
 <span data-ttu-id="7a319-115">**.NET framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7a319-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7a319-116">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7a319-116">See Also</span></span>  
 [<span data-ttu-id="7a319-117">元数据结构</span><span class="sxs-lookup"><span data-stu-id="7a319-117">Metadata Structures</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-structures.md)  
 [<span data-ttu-id="7a319-118">IMetaDataEmit 接口</span><span class="sxs-lookup"><span data-stu-id="7a319-118">IMetaDataEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)  
 [<span data-ttu-id="7a319-119">IMetaDataImport 接口</span><span class="sxs-lookup"><span data-stu-id="7a319-119">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)