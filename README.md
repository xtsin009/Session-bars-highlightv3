將非交易時間highlight

//@version=6
//This is the first Version*********************************************
// indicator('Session bars v2', '', true)
// timeRange = input.string('0915-1630', title="Time Range")
// inSession = na(time(timeframe.period, timeRange))
// bool frame = false
// frame := timeframe.period == 'D' or timeframe.period == 'W' or timeframe.period == 'M'
// bgcolor(frame ? na : inSession ? color.new(color.green, 60) : na)

//@version=6
// indicator('Session bars v2 簡化版', '', true) // 疊加在主K線，指標名自定
// timeRange = input.string('0915-1630', title="交易時段") // 自定時段 HHMM-HHMM
// // 核心1：判斷當前周期是否>2小時 → 是則frame=true（屏蔽背景色）
// frame = timeframe.period == 'H' and timeframe.multiplier > 2 or timeframe.isdaily or timeframe.isweekly or timeframe.ismonthly
// // 核心2：判斷當前K線是否在指定時段內
// inSession = not na(time(timeframe.period, timeRange))
// // 繪製背景色：僅小於等於2H周期 + 時段內，才顯示淺綠半透明背景
// bgcolor(not frame and inSession ? na: color.new(#4caf4f, 77) )
