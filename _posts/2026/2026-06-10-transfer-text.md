---
layout: default
title: Transfer Text
---

# Transfer Text

SELECT CAST(SUBSTRING(MEMO, 8, LEN(MEMO) - 7) as int) ID_ORD, oln.ID_ORD, imh.*  FROM tst.IMHIST imh left join (
 SELECT ID_ORD, ID_ITEM, ID_LOC FROM tst.CP_ORDLIN
 union
 SELECT ID_ORD, ID_ITEM, ID_LOC FROM tst.CP_INVLIN
 union
 SELECT ID_ORD, ID_ITEM, ID_LOC FROM tst.CP_INVLIN_HIST
) oln
  on CAST(SUBSTRING(imh.MEMO, 8, LEN(imh.MEMO) - 7) as int) = oln.ID_ORD and imh.ID_ITEM = oln.ID_ITEM and imh.ID_LOC = oln.ID_LOC
where CODE_DTL = 11 and QTY_ONHD_CHG < 0
 and oln.ID_ORD is NULL
  
<div class="datenote">
    <span>尹永贤</span><br>
    <span>2026-06-10</span><br>
    <span>上海</span>
</div>
