state={} state.a="[开启]" state.b="[开启]" state.c="[开启]" state.d="[开启]"

function SearchWrite(Search, Write, Type)    gg.clearResults()    gg.setVisible(false)    gg.searchNumber(Search[1][1], Type)    local count = gg.getResultCount()    local result = gg.getResults(count)    gg.clearResults()    local data = {}     local base = Search[1][2]        if (count > 0) then        for i, v in ipairs(result) do            v.isUseful = true         end                for k=2, #Search do            local tmp = {}            local offset = Search[k][2] - base             local num = Search[k][1]                         for i, v in ipairs(result) do                tmp[#tmp+1] = {}                 tmp[#tmp].address = v.address + offset                  tmp[#tmp].flags = v.flags              end                        tmp = gg.getValues(tmp)                         for i, v in ipairs(tmp) do                if ( tostring(v.value) ~= tostring(num) ) then                     result[i].isUseful = false                 end            end        end          for i, v in ipairs(result) do            if (v.isUseful) then                 data[#data+1] = v.address            end        end                if (#data > 0) then           gg.toast("搜索到"..#data.."条数据")           local t = {}           local base = Search[1][2]           for i=1, #data do               for k, w in ipairs(Write) do                   offset = w[2] - base                   t[#t+1] = {}                   t[#t].address = data[i] + offset                   t[#t].flags = Type                   t[#t].value = w[1]                                      if (w[3] == true) then                       local item = {}                       item[#item+1] = t[#t]                       item[#item].freeze = true                       gg.addListItems(item)                   end                                  end           end           gg.setValues(t)        else            gg.toast("not found", false)            return false        end    else        gg.toast("Not Found")        return false    end end function Fxs(Search, Write,Neicun,Mingcg,Shuzhiliang)  gg.clearResults()  gg.setRanges(Neicun)  gg.setVisible(false)  gg.searchNumber(Search[1][1], Search[1][3])  local count = gg.getResultCount()  local result = gg.getResults(count)  gg.clearResults()  local data = {}   local base = Search[1][2]    if (count > 0) then  for i, v in ipairs(result) do  v.isUseful = true  end  for k=2, #Search do  local tmp = {}  local offset = Search[k][2] - base   local num = Search[k][1]    for i, v in ipairs(result) do  tmp[#tmp+1] = {}  tmp[#tmp].address = v.address + offset  tmp[#tmp].flags = Search[k][3]  end    tmp = gg.getValues(tmp)    for i, v in ipairs(tmp) do  if ( tostring(v.value) ~= tostring(num) ) then  result[i].isUseful = false  end  end  end    for i, v in ipairs(result) do  if (v.isUseful) then  data[#data+1] = v.address  end  end  if (#data > 0) then  gg.toast(Mingcg.."开启成功"..#data.."")  local t = {}  local base = Search[1][2]  if Shuzhiliang == "" and Shuzhiliang > 0 and Shuzhiliang < #data then   Shuzhiliang=Shuzhiliang  else  Shuzhiliang=#data  end  for i=1, Shuzhiliang do  for k, w in ipairs(Write) do  offset = w[2] - base  t[#t+1] = {}  t[#t].address = data[i] + offset  t[#t].flags = w[3]  t[#t].value = w[1]  if (w[4] == true) then  local item = {}  item[#item+1] = t[#t]  item[#item].freeze = true  gg.addListItems(item)  end  end  end  gg.setValues(t)  gg.toast(Mingcg.."开启成功"..#t.."")     gg.addListItems(t)  else  gg.toast(Mingcg.."开启失败", false)  return false  end  else  gg.toast("开启失败")  return false  end end   local L0_0  L0_0 = 0  function SearchWrite(Search,Write,Type)  gg.clearResults() gg.setVisible(false) gg.searchNumber(Search[1][1],Type) local count=gg.getResultCount() local result=gg.getResults(count) gg.clearResults()  local data={} local base=Search[1][2] if(count>0)then for i,v in ipairs(result)do  v.isUseful=true end for k=2,#Search do local tmp={} local offset=Search[k][2]-base local num=Search[k][1] for i,v in ipairs(result)do tmp[#tmp+1]={} tmp[#tmp].address=v.address+offset tmp[#tmp].flags=v.flags  end tmp=gg.getValues(tmp) for i,v in ipairs(tmp)do if(tostring(v.value)~=tostring(num))then result[i].isUseful=false end end end for i,v in ipairs(result)do if(v.isUseful)then data[#data+1]=v.address  end end if(#data>0)then gg.toast(Name.."共搜索到"..#data.."个数据") local t={} local base=Search[1][2] for i=1,#data do for k,w in ipairs(Write)do  offset=w[2]-base t[#t+1]={} t[#t].address=data[i]+offset t[#t].flags=Type t[#t].value=w[1] if(w[3]==true)then local item={} item[#item+1]=t[#t] item[#item].freeze=true gg.addListItems(item) end end end gg.setValues(t) gg.sleep(500) gg.toast(Name.."开启成功,共修改"..#t.."条数据") else gg.toast(Name.."副特征码错误or脸丑\n或者是已经开启过了") return false end else gg.toast(Name.."主特征码错误or脸丑\n或者是已经开启过了") return false end end   function split(szFullString, szSeparator)   local nFindStartIndex = 1   local nSplitIndex = 1   local nSplitArray = {}   while true do   local nFindLastIndex = string.find  (szFullString, szSeparator, nFindStartIndex)   if not nFindLastIndex then   nSplitArray[nSplitIndex] =   string.sub(szFullString, nFindStartIndex, string.len  (szFullString))   break end   nSplitArray[nSplitIndex] = string.sub  (szFullString, nFindStartIndex, nFindLastIndex - 1)   nFindStartIndex = nFindLastIndex + string.len  (szSeparator)   nSplitIndex = nSplitIndex + 1 end return   nSplitArray end   function xgxc(szpy, qmxg)   for x = 1, #(qmxg) do   xgpy = szpy + qmxg[x]["offset"]   xglx = qmxg[x]["type"]   xgsz = qmxg[x]["value"]   xgdj = qmxg[x]["freeze"]   if xgdj == nil or xgdj == "" then   gg.setValues({[1]   = {address = xgpy, flags = xglx, value = xgsz}})   else   gg.addListItems({[1]   = {address = xgpy, flags = xglx,   freeze = xgdj, value = xgsz}}) end   xgsl = xgsl + 1 xgjg = true end end   function xqmnb(qmnb)   gg.clearResults()   gg.setRanges(qmnb[1]["memory"])   gg.searchNumber(qmnb[3]["value"], qmnb[3]["type"])   if gg.getResultCount() == 0 then   gg.toast(qmnb[2]["name"] .. "开启失败")   else   gg.refineNumber(qmnb[3]["value"], qmnb[3]["type"])  gg.refineNumber(qmnb[3]["value"], qmnb[3]["type"])   gg.refineNumber(qmnb[3]["value"], qmnb[3]["type"])   if gg.getResultCount() == 0 then   gg.toast(qmnb[2]["name"] .. "开启失败")   else           sl = gg.getResults(999999)   sz = gg.getResultCount()           xgsl = 0 if sz > 999999 then   sz = 999999 end for i = 1, sz do   pdsz = true for v = 4, #(qmnb) do if   pdsz == true then   pysz = {} pysz[1]   = {} pysz[1].address   = sl[i].address + qmnb[v]["offset"] pysz[1].flags   = qmnb[v]["type"]   szpy = gg.getValues(pysz)   pdpd = qmnb[v]["lv"] .. ";" .. szpy[1].value szpd   = split(pdpd, ";") tzszpd   = szpd[1] pyszpd = szpd[2]   if tzszpd == pyszpd then   pdjg = true pdsz = true else   pdjg = false pdsz = false end end end if   pdjg == true then szpy   = sl[i].address xgxc(szpy, qmxg) end end   if xgjg == true then   gg.toast(qmnb[2]["name"] .. "开启成功,共修改" .. xgsl .. "条数据")   else   gg.toast(qmnb[2]["name"] .. "开启失败")   end   end   end   end  function edit(orig,ret)_om=orig[1].memory or orig[1][1]_ov=orig[3].value or orig[3][1]_on=orig[2].name or orig[2][1]gg.clearResults()gg.setRanges(_om)gg.searchNumber(_ov,orig[3].type or orig[3][2])sz=gg.getResultCount()if sz<1 then gg.toast(_on.."开启失败")else sl=gg.getResults(720)for i=1,sz do ist=true for v=4,#orig do if ist==true and sl[i].value==_ov then cd={{}}cd[1].address=sl[i].address+(orig[v].offset or orig[v][2])cd[1].flags=orig[v].type or orig[v][3]szpy=gg.getValues(cd)cdlv=orig[v].lv or orig[v][1]cdv=szpy[1].value if cdlv==cdv then pdjg=true ist=true else pdjg=false ist=false end end end if pdjg==true then szpy=sl[i].address for x=1,#(ret)do xgpy=szpy+(ret[x].offset or ret[x][2])xglx=ret[x].type or ret[x][3]xgsz=ret[x].value or ret[x][1]xgdj=ret[x].freeze or ret[x][4]xgsj={{address=xgpy,flags=xglx,value=xgsz}}if xgdj==true then xgsj[1].freeze=xgdj gg.addListItems(xgsj)else gg.setValues(xgsj)end end xgjg=true end end if xgjg==true then gg.toast(_on.."开启成功")else gg.toast(_on.."开启失败")end end end function SearchWrite(Search, Write, Type) gg.clearResults() gg.setVisible(false) gg.searchNumber(Search[1][1], Type) local count = gg.getResultCount() local result = gg.getResults(count) gg.clearResults() local data = {} local base = Search[1][2] if (count > 0) then for i, v in ipairs(result) do v.isUseful = true end for k=2, #Search do local tmp = {} local offset = Search[k][2] - base local num = Search[k][1] for i, v in ipairs(result) do tmp[#tmp+1] = {} tmp[#tmp].address = v.address + offset tmp[#tmp].flags = v.flags end tmp = gg.getValues(tmp) for i, v in ipairs(tmp) do if ( tostring(v.value) ~= tostring(num) ) then result[i].isUseful = false end end end for i, v in ipairs(result) do if (v.isUseful) then data[#data+1] = v.address end end if (#data > 0) then gg.toast("搜索到"..#data.."条数据") local t = {} local base = Search[1][2] for i=1, #data do for k, w in ipairs(Write) do offset = w[2] - base t[#t+1] = {} t[#t].address = data[i] + offset t[#t].flags = Type t[#t].value = w[1] if (w[3] == true) then local item = {} item[#item+1] = t[#t] item[#item].freeze = true gg.addListItems(item) end end end gg.setValues(t) gg.toast("已修改"..#t.."条数据") gg.addListItems(t) else gg.toast("not found", false) return false end else gg.toast("Not Found") return false end end function split(szFullString, szSeparator) local nFindStartIndex = 1 local nSplitIndex = 1 local nSplitArray = {} while true do local nFindLastIndex = string.find(szFullString, szSeparator, nFindStartIndex) if not nFindLastIndex then nSplitArray[nSplitIndex] = string.sub(szFullString, nFindStartIndex, string.len(szFullString)) break end nSplitArray[nSplitIndex] = string.sub(szFullString, nFindStartIndex, nFindLastIndex - 1) nFindStartIndex = nFindLastIndex + string.len(szSeparator) nSplitIndex = nSplitIndex + 1 end return nSplitArray end function xgxc(szpy, qmxg) for x = 1, #(qmxg) do xgpy = szpy + qmxg[x]["offset"] xglx = qmxg[x]["type"] xgsz = qmxg[x]["value"] xgdj = qmxg[x]["freeze"] if xgdj == nil or xgdj == "" then gg.setValues({[1] = {address = xgpy, flags = xglx, value = xgsz}}) else gg.addListItems({[1] = {address = xgpy, flags = xglx, freeze = xgdj, value = xgsz}}) end xgsl = xgsl + 1 xgjg = true end end function xqmnb(qmnb) gg.clearResults() gg.setRanges(qmnb[1]["memory"]) gg.searchNumber(qmnb[3]["value"], qmnb[3]["type"]) if gg.getResultCount() == 0 then gg.toast(qmnb[2]["name"] .. "开启失败") else gg.refineNumber(qmnb[3]["value"], qmnb[3]["type"]) gg.refineNumber(qmnb[3]["value"], qmnb[3]["type"]) gg.refineNumber(qmnb[3]["value"], qmnb[3]["type"]) if gg.getResultCount() == 0 then gg.toast(qmnb[2]["name"] .. "开启失败") else sl = gg.getResults(999999) sz = gg.getResultCount() xgsl = 0 if sz > 999999 then sz = 999999 end for i = 1, sz do pdsz = true for v = 4, #(qmnb) do if pdsz == true then pysz = {} pysz[1] = {} pysz[1].address = sl[i].address + qmnb[v]["offset"] pysz[1].flags = qmnb[v]["type"] szpy = gg.getValues(pysz) pdpd = qmnb[v]["lv"] .. ";" .. szpy[1].value szpd = split(pdpd, ";") tzszpd = szpd[1] pyszpd = szpd[2] if tzszpd == pyszpd then pdjg = true pdsz = true else pdjg = false pdsz = false end end end if pdjg == true then szpy = sl[i].address xgxc(szpy, qmxg) end end if xgjg == true then gg.toast(qmnb[2]["name"] .. "开启成功,共修改" .. xgsl .. "条数据") else gg.toast(qmnb[2]["name"] .. "开启失败") end end end end  function SearchWrite(Search, Write, Type) gg.clearResults()    gg.setVisible(false)    gg.searchNumber(Search[1][1], Type)    local count = gg.getResultCount()    local result = gg.getResults(count)    gg.clearResults()   local data = {}     local base = Search[1][2]        if (count > 0) then        for i, v in ipairs(result) do            v.isUseful = true         end               for k=2, #Search do            local tmp = {}            local offset = Search[k][2] - base             local num = Search[k][1]                         for i, v in ipairs(result) do                tmp[#tmp+1] = {}                 tmp[#tmp].address = v.address + offset                  tmp[#tmp].flags = v.flags              end                        tmp = gg.getValues(tmp)                         for i, v in ipairs(tmp) do                if ( tostring(v.value) ~= tostring(num) ) then                     result[i].isUseful = false end end end for i, v in ipairs(result) do if (v.isUseful) then data[#data+1] = v.address end end if (#data > 0) then gg.toast("✨开启成功✨"..#data.."") local t = {} local base = Search[1][2] for i=1, #data do for k, w in ipairs(Write) do offset = w[2] - base t[#t+1] = {} t[#t].address = data[i] + offset t[#t].flags = Type t[#t].value = w[1] if (w[3] == true) then local item = {} item[#item+1] = t[#t] item[#item].freeze = true gg.addListItems(item) end end end gg.setValues(t) else gg.toast("", false) return false end else gg.toast("") return false end end local app = {} function Assert(data) if data == nil or data == "" or data == "nil" then return false else return true end end function mearrass(memory, array) if Assert(memory) and Assert(array) then return true else return false end end function typetab(array, type) local datatype = {} for i = 1, #array do if Assert(array[i].type) then table.insert(datatype, i, array[i].type) else if Assert(type) then table.insert(datatype, i, type) else return false end end end return true, datatype end function app.memorysearch(memory, array, type) gg.setVisible(false) local rx = mearrass(memory, array) if rx then local rx, datatype = typetab(array, type) if rx then if Assert(array[1].hv) then gg.clearResults() gg.setRanges(memory) gg.searchNumber(array[1].lv .. "~" .. array[1].hv, datatype[1]) elsegg.clearResults() gg.setRanges(memory) gg.searchNumber(array[1].lv, datatype[1]) end if gg.getResultCount() == 0 then return false else local tab = {} local data = gg.getResults(gg.getResultCount()) gg.clearResults() for i = 1, #data do data[i].rx = true end for i = 2, #array do local t = {} local offset = array[i].offset for x = 1, #data do t[#t + 1] = {} t[#t].address = data[x].address + offset t[#t].flags = datatype[i] end local t = gg.getValues(t) for z = 1, #t do if Assert(array[i].hv) then if tonumber(t[z].value) < tonumber(array[i].lv) or tonumber(t[z].value) > tonumber(array[i].hv) then data[z].rx = false end else if tostring(t[z].value) ~= tostring(array[i].lv) then data[z].rx = false end end end end for i = 1, #data do if data[i].rx then tab[#tab + 1] = data[i].address end end if #tab > 0 then return true, tab else return false end end else print("type参数错误") gg.toast("type参数错误") os.exit() end else print("memory or array参数错误") gg.toast("memory or array参数错误") os.exit() end end function app.memoryread(addr, type) local t = {} t[1] = {} t[1].address = addr t[1].flags = type if #t > 0 then return true, gg.getValues(t)[1].value else return false end end function app.memorywrite(addr, type, value, freeze) local t = {} t[1] = {} t[1].address = addr t[1].flags = type t[1].value = value if #t > 0 then if Assert(freeze) then t[1].freeze = freeze return gg.addListItems(t) else return gg.setValues(t) end else return false end end function split(szFullString, szSeparator) local nFindStartIndex = 1 local nSplitIndex = 1 local nSplitArray = {} while true do local nFindLastIndex = string.find(szFullString, szSeparator, nFindStartIndex) if not nFindLastIndex then nSplitArray[nSplitIndex] = string.sub(szFullString, nFindStartIndex, string.len(szFullString)) break end nSplitArray[nSplitIndex] = string.sub(szFullString, nFindStartIndex, nFindLastIndex - 1) nFindStartIndex = nFindLastIndex + string.len(szSeparator) nSplitIndex = nSplitIndex + 1 end return nSplitArray end function xgxc(szpy, qmxg) for x = 1, #(qmxg) do xgpy = szpy + qmxg[x]["offset"] xglx = qmxg[x]["type"] xgsz = qmxg[x]["value"] gg.setValues({[1] = {address = xgpy, flags = xglx, value = xgsz}}) xgsl = xgsl + 1 end end function xqmnb(qmnb) gg.clearResults() gg.setRanges(qmnb[1]["memory"]) gg.searchNumber(qmnb[3]["value"], qmnb[3]["type"]) if gg.getResultCount() == 0 then gg.toast(qmnb[2]["name"] .. "开启失败") else gg.refineNumber(qmnb[3]["value"], qmnb[3]["type"]) gg.refineNumber(qmnb[3]["value"], qmnb[3]["type"]) gg.refineNumber(qmnb[3]["value"], qmnb[3]["type"]) if gg.getResultCount() == 0 then gg.toast(qmnb[2]["name"] .. "开启失败") else sl = gg.getResults(999999) sz = gg.getResultCount() xgsl = 0 if sz > 999999 then sz = 999999 end for i = 1, sz do pdsz = true for v = 4, #(qmnb) do if pdsz == true then pysz = {} pysz[1] = {} pysz[1].address = sl[i].address + qmnb[v]["offset"] pysz[1].flags = qmnb[v]["type"] szpy = gg.getValues(pysz) pdpd = qmnb[v]["lv"] .. ";" .. szpy[1].value szpd = split(pdpd, ";") tzszpd = szpd[1] pyszpd = szpd[2] if tzszpd == pyszpd then pdjg = true pdsz = true else pdjg = false pdsz = false end end end if pdjg == true then szpy = sl[i].address xgxc(szpy, qmxg) xgjg = true end end if xgjg == true then gg.toast(qmnb[2]["name"] .. "开启成功,共修改" .. xgsl .. "条ΔΘ") else gg.toast(qmnb[2]["name"] .. "开启失败") end end end end function Fxs(Search, Write,Neicun,Mingcg,Shuzhiliang)  gg.clearResults()  gg.setRanges(Neicun)  gg.setVisible(false)  gg.searchNumber(Search[1][1], Search[1][3])  local count = gg.getResultCount()  local result = gg.getResults(count)  gg.clearResults()  local data = {}   local base = Search[1][2]    if (count > 0) then  for i, v in ipairs(result) do  v.isUseful = true  end  for k=2, #Search do  local tmp = {}  local offset = Search[k][2] - base   local num = Search[k][1]    for i, v in ipairs(result) do  tmp[#tmp+1] = {}  tmp[#tmp].address = v.address + offset  tmp[#tmp].flags = Search[k][3]  end    tmp = gg.getValues(tmp)    for i, v in ipairs(tmp) do  if ( tostring(v.value) ~= tostring(num) ) then  result[i].isUseful = false  end  end  end    for i, v in ipairs(result) do  if (v.isUseful) then  data[#data+1] = v.address  end  end  if (#data > 0) then  gg.toast(Mingcg.."搜索到"..#data.."条数据")  local t = {}  local base = Search[1][2]  if Shuzhiliang == "" and Shuzhiliang > 0 and Shuzhiliang < #data then   Shuzhiliang=Shuzhiliang  else  Shuzhiliang=#data  end  for i=1, Shuzhiliang do  for k, w in ipairs(Write) do  offset = w[2] - base  t[#t+1] = {}  t[#t].address = data[i] + offset  t[#t].flags = w[3]  t[#t].value = w[1]  if (w[4] == true) then  local item = {}  item[#item+1] = t[#t]  item[#item].freeze = true  gg.addListItems(item)  end  end  end  gg.setValues(t)  gg.toast(Mingcg.."已修改"..#t.."条数据")     gg.addListItems(t)  else  gg.toast(Mingcg.."开启失败", false)  return false  end  else  gg.toast("搜索失败")  return false  end end  

 sj = (os.date("%Y年%m月%d日%H时%M分%S秒"))  

gg.alert("请在游戏中运行脚本，否则无法识别游戏区服","好") if gg.getTargetPackage()=="com.tencent.iglite" and "com.tencent.iglitece" and "com.tencent.tmgp.pubgmhd" then QW="8" else QW="16384" end

function YONEX()

end

function setvalue(address,flags,value) YONEX('Modify address value(Address, value type, value to be modified)') local tt={} tt[1]={} tt[1].address=address tt[1].flags=flags tt[1].value=value gg.setValues(tt) end

---yonex

--0

gg.alert("ONLY for YONEX Android 10 ")

function HOME()

  MN = gg.multiChoice({

      " BYPASS",

      " wallhack 720G",

      " parachute fly ",

      " aimbot OP",

      " MAGIC ULTA+ head FOR YONEX",

      " NO RECOIL(lobby 1time)",

      "  FLY BOLTI PUBLIC",

      " FLASH",

      " wallshoot ",

      " EXIT ",

}, nil, "personal SCRIPT FOR MR YONEX\n\n \n DATE" .. Time)

  if MN == nil then

else

if MN[1] == true then A1()end

if MN[2] == true then A2()end

if MN[3] == true then A3()end

if MN[4] == true then A4()end

if MN[5] == true then A5()end

if MN[6] == true then A6()end

if MN[7] == true then A7()end

if MN[8] == true then A8()end

if MN[9] == true then A9()end

if MN[10] == true then EXIT()end

end

PUBGMH = -1

end-- YX

function A1()

gg.setVisible(true)

gg.toast(" YONEX BOLTI PUBLIC")

gg.setVisible(false)

gg.searchNumber("135682;144387", gg.TYPE_DWORD)

gg.refineNumber("135682", gg.TYPE_DWORD)

gg.getResults(50000)

gg.setVisible(false)

gg.editAll("0", gg.TYPE_DWORD)

gg.setVisible(false)

gg.clearResults()

gg.clearResults()

gg.setRanges(gg.REGION_C_ALLOC)

gg.setVisible(false)

gg.searchNumber("134658;131586", gg.TYPE_DWORD)

gg.refineNumber("134658", gg.TYPE_DWORD)

gg.getResults(50000)

gg.setVisible(false)

gg.editAll("0", gg.TYPE_DWORD)

gg.setVisible(false)

gg.clearResults()

gg.clearResults()

gg.setRanges(gg.REGION_C_ALLOC)

gg.setVisible(false)

gg.searchNumber("4096;135682", gg.TYPE_DWORD)

gg.refineNumber("4096", gg.TYPE_DWORD)

gg.getResults(50000)

gg.setVisible(false)

gg.editAll("0", gg.TYPE_DWORD)

gg.setVisible(false)

gg.clearResults()

gg.setVisible(false)

gg.clearResults()

gg.setRanges(gg.REGION_C_ALLOC)

gg.clearResults()

gg.setRanges(gg.REGION_C_ALLOC)

gg.searchNumber("157567", gg.TYPE_DWORD)

gg.getResults(50000)

gg.editAll("0", gg.TYPE_DWORD)

gg.clearResults()

gg.clearResults()

gg.setRanges(gg.REGION_C_ALLOC)

gg.searchNumber("135938", gg.TYPE_DWORD)

gg.getResults(50000)

gg.editAll("0", gg.TYPE_DWORD)

gg.clearResults()

gg.clearResults()

gg.setRanges(gg.REGION_C_ALLOC)

gg.searchNumber("135170", gg.TYPE_DWORD)

gg.getResults(50000)

gg.editAll("0", gg.TYPE_DWORD)

gg.clearResults()

gg.setRanges(gg.REGION_C_ALLOC)

gg.searchNumber("135426", gg.TYPE_DWORD)

gg.getResults(50000)

gg.editAll("0", gg.TYPE_DWORD)

gg.clearResults()

gg.setRanges(gg.REGION_C_ALLOC)

gg.searchNumber("135212", gg.TYPE_DWORD)

gg.getResults(50000)

gg.editAll("0", gg.TYPE_DWORD)

gg.clearResults()

gg.clearResults()

gg.setRanges(gg.REGION_C_ALLOC)

gg.setVisible(false)

gg.searchNumber("134914;262403", gg.TYPE_DWORD)

gg.refineNumber("134914", gg.TYPE_DWORD)

gg.getResults(50000)

gg.setVisible(false)

gg.editAll("0", gg.TYPE_DWORD)

gg.setVisible(false)

gg.clearResults()

gg.setRanges(gg.REGION_C_ALLOC)

gg.setVisible(false)

gg.searchNumber("133378;262403", gg.TYPE_DWORD)

gg.refineNumber("133378", gg.TYPE_DWORD)

gg.getResults(50000)

gg.setVisible(false)

gg.editAll("0", gg.TYPE_DWORD)

gg.setVisible(false)

gg.clearResults()

gg.setRanges(gg.REGION_C_ALLOC)

gg.setVisible(false)

gg.searchNumber("131330;133634", gg.TYPE_DWORD)

gg.refineNumber("131330", gg.TYPE_DWORD)

gg.getResults(50000)

gg.setVisible(false)

gg.editAll("0", gg.TYPE_DWORD)

gg.setVisible(false)

gg.clearResults()

gg.setRanges(gg.REGION_C_ALLOC)

gg.setVisible(false)

gg.searchNumber("131842;132098", gg.TYPE_DWORD)

gg.refineNumber("131842", gg.TYPE_DWORD)

gg.getResults(50000)

gg.setVisible(false)

gg.editAll("0", gg.TYPE_DWORD)

gg.setVisible(false)

gg.clearResults()

gg.setRanges(gg.REGION_C_ALLOC)

gg.searchNumber("133634", gg.TYPE_DWORD)

gg.getResults(50000)

gg.editAll("0", gg.TYPE_DWORD)

gg.clearResults()

gg.clearResults()

gg.setRanges(gg.REGION_C_ALLOC)

gg.searchNumber("132098", gg.TYPE_DWORD)

gg.getResults(50000)

gg.editAll("0", gg.TYPE_DWORD)

gg.alert("New BYPASS Activated ")

end

  

function A2()

gg.clearResults()

gg.setRanges(gg.REGION_VIDEO)

gg.searchNumber("1.12126335e-19;3.64337601e-44;2.0:13", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)

gg.refineNumber("2", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)

revert = gg.getResults(5, nil, nil, nil, nil, nil, nil, nil, nil)

gg.editAll("120", gg.TYPE_FLOAT)

gg.clearResults()

gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)

gg.searchNumber("2.2509765625;2.0:485", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1, 0)

revert = gg.getResults(50, nil, nil, nil, nil, nil, nil, nil, nil)

gg.editAll("130", gg.TYPE_FLOAT)

gg.clearResults()

gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)

gg.searchNumber("8200;8201", gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1, 0)

revert = gg.getResults(50, nil, nil, nil, nil, nil, nil, nil, nil)

gg.editAll("7", gg.TYPE_DWORD)

gg.clearResults()

gg.toast("wh+ch 720G by ngyt")

end

function A3()

 MN3 = gg.multiChoice({

      "loby needed ",

      " on plane ",

      " fast parachute";

      " Back",

}, nil, "                YONEX GAMING")

if MN2 == nil then

else

if MN3[1] == true then P1()end

if MN3[2] == true then P2()end

if MN3[3] == true then P3()end

if MN3[4] == true then HOME()end

end

PUBGMH = -1

end

 

function P1()

gg.setRanges(gg.REGION_C_ALLOC)

gg.setVisible(false)

gg.searchNumber("100.0;1", gg.TYPE_FLOAT)

gg.searchNumber("100.0", gg.TYPE_FLOAT)

gg.getResults("100")

gg.editAll("2", gg.TYPE_FLOAT)                               

 end

 

function P2()

gg.setRanges(gg.REGION_ANONYMOUS)

gg.searchNumber("1024;3000", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)

gg.getResults("100")

gg.editAll("9999999", gg.TYPE_FLOAT)

gg.toast("����SUCCESSFUL ACTIVATED����")

end

 function P3()

 gg.clearResults()

 gg.setRanges(gg.REGION_C_BSS)

gg.searchNumber("2048D;4D;1F;1F;1D:30", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)

gg.getResultsCount()

gg.clearResults()

gg.setRanges(gg.REGION_ANONYMOUS)

gg.searchNumber("3000;5000;1024;1000::", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)

gg.getResults(3472849)

gg.editAll("999999", gg.TYPE_FLOAT)

gg.toast(" parachute")

 

end

 

          

  

function A4()

so=gg.getRangesList('libUE4.so')[1].start

py=0x18D8944

setvalue(so+py,16,9999)

gg.toast(" 💘 ᴀɪᴍʙᴏᴛ 100% 💘")

end--Yonex 

  

  

function A5()

gg.alert(" sabar Karo 😂🤣🤣😂🤣😂 ")

end

function A6()

so=gg.getRangesList('libUE4.so')[1].start

py=0xD7242C

setvalue(so+py,16,0)

gg.alert(" Done ")

end

function A7()

gg.alert(" Done ")

end

function A8()

  MN2 = gg.multiChoice({

      "damage (FIX) ",

      "FLASH ON",

      "FLAH OFF",

      "unlimited fuel",

      " Speed HACK 0.19.0",

      "back",

}, nil, "           Speed Menu for YONEX GAMING")

if MN2 == nil then

else

if MN2[1] == true then M1()end

if MN2[2] == true then M2()end

if MN2[3] == true then M3()end

if MN2[4] == true then M4()end

if MN2[5] == true then M5()end

if MN2[6] == true then HOME()end

end

PUBGMH = -1

end

function M1()

gg.alert(" Done ")

end

end

function M2()

so=gg.getRangesList('libUE4.so')[1].start

py=0x2BA788C

setvalue(so+py,16,8.5)

gg.toast(" Anti lag flash On ")

end

  

function M3()

so=gg.getRangesList('libUE4.so')[1].start

py=0x2BA788C

setvalue(so+py,16,10.5)

gg.toast("  ғʟᴀsʜ ᴏf")

end

 

    

function M4()

gg.alert(" Done ")

end

function M5()

gg.alert(" Done ")

 

end

function A9()

gg.alert(" Done ")

end

function EXIT()

print("  YONEX  \n     SUBSCRIBE Telegram channel : @yonexgaming\n   ")

print("HACK ONLY PUBG LITE")

  gg.skipRestoreState()

gg.setVisible(true)

os.exit()

end

while true do

  Time = os.date("%G-%m-%d | TIME: %H:%M:%S")

  if gg.isVisible(true) then

    PUBGMH = 1

    gg.setVisible(false)

  end--I

  gg.clearResults()

  if PUBGMH == 1 then

    HOME()

  end--I

end--W



























