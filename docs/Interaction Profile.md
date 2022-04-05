An Interaction Profile is a collection of one or more devices which will be used together. For example `Xbox One Controller`,  `Mouse and Keyboard`, and  `Valve Index Controllers` are all standard interaction profiles.

Multiple interaction profiles can be used at once to allow for mixed input. However more advanced users can take this further by creating custom interaction profiles. For example two mice, or a Dualsense with floor pedals and back buttons. 

Binding Layouts targeting a certain interaction profile can be automatically converted to other similar interaction profiles. For example, if an application only has default bindings for an Xbox 360 controller SuInput will be able to convert those bindings to target almost any other generic controller. Once the bindings have been converted they can be edited as if they targeted the other interaction profile.

Interaction profiles are also in command of what input glyphs the game uses. 

### Gameplay Semantic Profile
- Delta2D, Turn Camera / Move Cursor (Mouse Delta, XInput Right Thumbstick)
- Axis2D, Move (WASD, XInput Left Thumbstick)
- Button, Attack (Mouse Left, XInput Right Trigger)
- Button, Use (Mouse Right, XInput Left Trigger)
- Button, Reload ('R', XInput 'X')
- Button, Jump (Space, XInput 'A')
- Button, Crouch (Ctrl, XInput 'B')
- Button, Sprint (Shift, XInput Left Thumbstick Click)
- Button, Menu (Escape, XInput Start)
- Button, Item Right (Scroll Up, XInput Right Bumper)
- Button, Item Left (Scroll Down, XInput Left Bumper)

### GUI Semantic Profile
- Delta2D, Scroll (Scroll wheel)
- Delta1D, Zoom (Trackpad Pinch, Ctrl + Scroll wheel)
- Button, Up (Up Key, XInput DPad Up, XInput Left Thumbstick Up)
- Button, Left (Left Key, XInput DPad Left, XInput Left Thumbstick Left)
- Button, Down (Down Key, XInput DPad Down, XInput Left Thumbstick Down)
- Button, Right (Right Key, XInput DPad Right, XInput Left Thumbstick Right)
- Button, Select (Mouse Left, Enter, XInput 'A')
- Button, Back (Backspace, XInput 'B')
- Button, Exit (Escape, XInput Menu)
- Button, Tab Right ('E', XInput Right Bumper)
- Button, Tab Left ('Q', XInput Left Bumper)
- Button, Menu Right ('D', XInput Right Trigger)
- Button, Menu Left ('A', XInput Left Trigger)

TODO sharing devices between players
TODO automatic device consumption
TODO automatic layout generation

<iframe border=0
	frameborder=0
	height=480
	width=720   src="https://viewer.diagrams.net/?tags=%7B%7D&highlight=0000ff&edit=_blank&layers=1&nav=1#R%3Cmxfile%3E%3Cdiagram%20id%3D%22h5Q61B0YN9rPFSDJiW0-%22%20name%3D%22Mixed%20Input%22%3E3VnLUtswFP2aLNuJLDuPJSEBOpCSFqbAqiNsxRajWI4iE7tfXzmW44fABEpiN6v4Hl29rs6RrpQOPF1E5xwF3pQ5mHaMrhN14LhjGKALB%2FInQeIUsXpmCricOMopB27IH5zVVGhIHLwqOQrGqCBBGbSZ72NblDDEOVuX3eaMlnsNkIs14MZGVEfviCO8FB0Y%2FRy%2FwMT1sp5Bb5iWLFDmrGay8pDD1gUITjrwlDMm0q9FdIppErwsLmm9s1dKtwPj2Be7VAjOgHW3Xv4m3ybhxSya%2Bye3j18sNTYRZxPGjpy%2FMhkXHnOZj%2BgkR0echb6Dk1a70sp9rhgLJAgk%2BISFiNViolAwCXliQVUpjoi4T6p%2FtZT1UCgZR6rljRErQ5%2BtCsCKhdzGNVPMWIO4i0WNn%2BJlMv9CByqW55gtsOCxdOCYIkGey%2FxAimbu1i9fCfmhFuMdC6PafUY0VD1d4viRIe5oK1Zej7VHBL4J0CYmaynKcuxfjeMz5gJHtTNXpRmh47K5zuUBMswrSKPX3VOo%2Bo1w2JdDL5A4MR8y4iZGTuON9e88Npri8abqCecoLjgEjPhiVWh5lgA5SaBZZgmo7k4Vf2BZdf7yIx1BTpPtVD7OHKPFIhu0TGW9%2F%2BWkOLwyYaPK1KXUq0jPqnAiHaiqVaHFJ6gKaqqasnCFG5fUNg4NSAotLTHnl%2FPv45%2BPv54cYxT2oixQx35wmbo8XgyH0aoEzKw5G7qK0N0ZZ3NCm6d2%2FxXFF6nd3xO1l8F1fA%2BEPeAsmF07ox%2BePc3S12On9nBHalutovZQo%2FY4RHSF%2FRZs0mbbbhegkcTn45QEu953QbtICfQb74yiGHOJ6bvJwdPxCi2315vmeGlp8ToJAkpsuVbMb13AzJeOpINmW%2BbRHUl1WdTb8gefLf8PvRNU7%2F3wjXeC6r0YfvI7QV1M63PBEfEd4rvy6wrFLBSNS3BYjqxxyC3rxTA284RwcAVazSpQk4wJKpKBu70HvFfKplUrzXZIWT81C7lv%2BzQMh5V0eI8ilmb%2Bb1Qa7%2Fw%2FPTj5Cw%3D%3D%3C%2Fdiagram%3E%3Cdiagram%20id%3D%22c1TGQ3jnEVbHoawuWCXP%22%20name%3D%22Sharing%22%3E7Vltd5owFP41fuwOEAH3UetL2609PfN02n3ZSSVCtkBYjCL79QslEF6crbMVtu6TuTc3CXnu89wE6YBzfzthMPSuqYNIx9CcbQcMO4aha6AnfhJPnHpMq5s6XIYdGaQcU%2FwTZSOld40dtCoFckoJx2HZuaBBgBa85IOM0agctqSkvGoIXVRzTBeQ1L0z7HAv9fYMW%2FkvEHa9bGXdep%2F2%2BDALljtZedChUcEFRh1wzijlacvfniOSgJfhgu3NVe%2FChEvzzrihl%2FNw8%2FnHWTrZ%2BJAh%2BRYYCvgfT%2F1pxKKJN7gcD2fgy0N4wR6u3LNsazzO8EKOgE%2BalHGPujSAZKS8A0bXgYOSWTVhqZiPlIbCqQvnN8R5LLkA15wKl8d9InvRFvN5MvydKa37Qs9wK2d%2BNGJpPBMCCdWKrtkC7dl3xkTIXMT3xEmWJKAU6CQBniDqI85iEcAQgRxvypyDkrpuHqfSIxoyQwdkS867gWQtV7qm6xWq5bCcocjDHE1D%2BAhIJFRezsZhyG4Q42i7FwvZ25PcknUjU1GkRKhnPq8gQEs7Hjx7MA7u4OLr2Hdu5hM%2FWn63RmdWI1QPxKMXuJ6Y9xm%2FE0Ox%2FdF6JbqDv5LuoEb3Dyh%2BoJA57WS8YbaM8noNp7dDebtO%2BZ0YaU1RfufT2P8z9mTGzFYVKft3Z7IGA1GnNFWytFtGl5i09LjWu%2BXildvF6mW%2FUvXafdsxmhDDYfg%2BeaLq3Zdmqxx6S7F4QJU%2BYJbS1wWVtKTyk6NUZvqMwbgQFiYBqwPWMStvHZV4cSjuixeN9AkUTXJMjmBO%2FeZwS2CMmPDVz8RWyK9yWwb2Ce8Oe4lbwLAfhgQvBEtp0E4QdatCtl7TKIJGathpDvTW1D6gn6b21dZpY%2B3L9l7QbcewiMjTwMEb0XSTZl4O806xWKG%2FnfrOddpEldx5F%2F2H5V28r%2B97c3q6DICXLgNHpayuj6knIKnc1Qc4cHDgimqgzfrTYTv1UP2LzWpaDr03LAfzmXIA7frHwTxUDv3ko0zau2qnLKrHxGvqQpjqC1B6hqvvaGD0Cw%3D%3D%3C%2Fdiagram%3E%3Cdiagram%20id%3D%2295kvRpUVmhsFwS-qhy79%22%20name%3D%22Copilot%22%3E3VrRcps4FP0aT5%2BSMQiw8xh7vWlm0pnMJjNt900GGbQRiAphm379XgkpGNMkTrtey81DgKuLpHN0dHUlPELzfHsjcJl94glhI3%2BcbEfoj5Hve2M0hYuyNK0ljILWkAqaGKfO8EC%2FE%2FumsdY0IVXPUXLOJC37xpgXBYllz4aF4Ju%2B24qzfqslTsnA8BBjNrR%2BponMWuvUn3T2j4SmmW3Zi67akiWOn1LB68K0V%2FCCtCU5ttUYjFWGE77ZMaHFCM0F57K9y7dzwhStlrHxxd%2FXj99X8lF6j59uK%2F71YnZ10Vb253teeQYnSCF%2FuuqvN3fh8q98Ie7jq6RYkLiU%2BAJFBptsLJUkAWbNIxcy4ykvMFt01pmmi6hqx%2FDU%2BdxxXoLRA%2BM%2FRMrGyATXkoMpkzkzpQfiMbgrXouYvALCDKXEIiXyFT%2FPgFUId2Rj6LohPCdSNOAgCMOSrvvawkai6bNfRzbcGL7fwb3p9hqz2rT0Zcm3YJnzQgrOGBGDwelTv8moJA8l1uxsYGb%2FCs1rIiTZvsqLKfWnZkaYYBGYx0038zw7abKdWReNj8SkjUJnrWLPxs03Zew7JWPb7x0d3zPcKPGOvcG4OCFgFPQFjKKTK9gfkHhdlozGMIC8OA8Wg%2FDULIZowOIpAsMK4rcp9KZHCBTRgYEidCxQRC8teLeFJALHrdTH94KvKCPnIXrv5KEDTZwQ%2FX8schQeuhq6ldTZfp9fVhd4jmV1dk%2FaE3bEoNlZQteqRUbTQhdE32q1C5sxspLdE9yl6moGAPaeFWewS%2FXHfLXS%2BcmHOS8p4%2FKD2u%2FBpljBzWicwZURqTxTnOs3pCBYquuGt1WZsaxa5FCl2jfCxlVViz2vuRwpstruLoXtirUAIRpD3%2Fo%2BWMet%2FTGjClZCcqBNCixbGjT8DW7UQ1VrprC6bSpJcs1MDVt3cOHiCS5K14qRh%2Fq2KGt5%2BVN9%2FgW4FgvRI6pwmoHax6U9KpqXIJDOa5MRoa5LLjP90prG2h9rsxYFUXDJFpYv1nQ1gWwu%2Fz9oQk%2FHF7DVFS1SZaZK9SpqACBaJGCtniVLcNwhVA611DGK6nma4XVbB6BTowxgdWv6n4bdtlyaxP9QOHtxECKV7Ac7q1Y9dmimohnkxOzamKVanH4YMPshdT8jg%2FyCzTkD5KpdFAWTaDoBO5DGn8hOCfICFAamhh37Sv8dIxrbA7hh9H227UZfND1a%2BL36DdIIu4i9mUYEoVNphO33%2BaURYehYGhEMDyHOUMf%2BoTpGbul4eK7h%2BuFQ5Lt2OBQMjzWcPxzaZ%2FH0h0NB8IPtxPkHhkP3yXYmuhIYXtwnz9rUFO7ucMN1GupopNhf6hxY64bflE6h8SMfgAaTQzU%2FdUvzw5O6M0nqIte%2B%2BIXD%2FPh3FPr0TIP78OTu5eA%2BHDgnJe%2BA5t1IYI6sefvR6u2Df88pzdt%2BH6J5F%2FW%2B%2F2HLP%2BK2Bx67n03psp2fpaHFvw%3D%3D%3C%2Fdiagram%3E%3Cdiagram%20id%3D%22_5Ky0LnrIYnmiXWjiXko%22%20name%3D%22Custom%20Interaction%20Profile%22%3E5VrbctowEP0aHpuxLV%2FgMSEkaZtMaOlMk74pWGC1wnKFHOx%2BfWUs4YtSAhOIxfQFvOuVbO%2Bes1qt3QPDRXbNYBLd0RCRnmOFWQ9c9hzHtkBf%2FBWavNR4vlsq5gyH0qhSTPAfpEZKbYpDtGwYckoJx0lTOaVxjKa8oYOM0VXTbEZJ86oJnCNNMZlComu%2F45BHpbbvBJX%2BBuF5pK5s%2B4PyzAIqY%2FkkywiGdFVTgVEPDBmlvDxaZENECucpv2Rf%2BI%2FBp1E6%2BfVteHNDf9Or%2B%2BBDOdnVPkM2j8BQzA87tSMfjefKXygU7pMiZTyicxpDMqq0F4ymcYiKWS0hVTa3lCZCaQvlT8R5LrEAU06FKuILIs%2BiDPOHYviZJ6XH2pnLTM68FnIp7OgC6aolTdkUbbEDEomQzdG2%2BSQWCqfU4CQdfI3oAnGWCwOGCOT4uYk5KKE739jJoeeMwbxmkFAc82Vt5nGhEAaShX2JwFxRqxXplrljedvsxUF5A0qqPUmlWqNnDyRJjz5DkkovfEb5E4Us1CDWBNAqwhxNEriO10okoSZY9gv8M2IcZVtDtXFSy0eluKpyhK1Molp%2B8K1%2Fx7bm4P3953bCxFjceo2Khfio6FcIFRnX0pHY6J0UGwFwzaejp9Hx4YlmQnMfI%2FE7pCKelBDEDGVnAM7aXuuYoP6pLJWGkDrolNQ6C%2B1WwndbQClvVI6qsLJvdmizPbCPT%2FZAI%2FsYhZAszeS27QZmMbv%2FHy%2B9gx1ZavuHpumbQjbQEH9XXHyYLjldiIOPMUcMTjmmsZDGjM6wCJuZdGhXou4LfAjekw92J7vCAwPb3nWLZ7tGIdvWN1JjAvOiULNsLS5mINhtLnkAdJ3RVUxrTjxPEoKnsMwIp%2BBFt3sv6lm2i8QwE3sVedLuHyFR%2BLsmCmBWovC16GyWv82CZ13gOMTxXBzdwpym%2FDSw73SOfaCn4Vs0K%2Br8O5ou9VLifStGZ6%2BS8cgE2rT1XyOQ6rkbQiA1cb2IfDG2RlDE9QxrWAJ9jf26vqwZFAmMosiuxahpFNGzoMEU8U3r6Tvd9AzN6Cw4uzYAgWMW5vVu2rq3cJlCUuU2s3sKnnE9BaeTJtuhIb1rt0yVr6ZAWt%2FImd5T8IzrKagbOKWeQtuL3fcUgF50d5EYjlzvqSXt9Xrv4G%2B%2F3hYdR4tOa9k7jX5CG%2FfH7CcIsfoGrHyjV31JB0Z%2FAQ%3D%3D%3C%2Fdiagram%3E%3C%2Fmxfile%3E"></iframe>

## Mixed Input
![Mixed Input Demo Diagram](device-diagram.drawio#0)

## Sharing
![Sharing Demo Diagram](device-diagram.drawio#1)

## Copilot
![Copilot Demo Diagram](device-diagram.drawio#2)

## Custom Interaction Profile
![Custom Interaction Profile Demo Diagram](device-diagram.drawio#3)
