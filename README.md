# YouTube Live Chat Overlay CSS for OBS

This custom CSS is designed to transform the popup URL of a YouTube live chat into a simple, lightweight, and transparent overlay for [OBS (Open Broadcaster Software)](https://github.com/obsproject/obs-studio). The CSS removes all unnecessary elements from the HTML, creating a clean and minimalistic chat overlay perfect for live streaming.

## Features

- **Transparent Background**: Ensures the chat area blends seamlessly with your stream.
- **Full Width and Height**: The chat area takes up the entire popup window, providing maximum visibility.
- **Owner Highlight**: Messages from the owner are highlighted with a distinct color.
- **Removal of Unnecessary Elements**: Strips away headers, footers, input areas, and other non-essential components to keep the chat overlay clean and focused.

## Installation

1. **Open YouTube Live Chat in a Popup**:
    - Go to your YouTube live stream page.
    - Open the chat in a popup window by clicking on the three dots in the top right corner of the chat and selecting "Popout chat."

2. **Add Custom CSS in OBS**:
    - In OBS, add a new browser source.
    - Paste the URL of your YouTube live chat popup.
    - Under "Custom CSS," paste the following code:

    ```css
	/* --- Transparent background --- */
	yt-live-chat-renderer {
		background-color: transparent !important;
	}

	/* --- Hide header and input --- */
	yt-live-chat-header-renderer,
	yt-live-chat-message-input-renderer,
	yt-live-chat-viewer-engagement-message-renderer,
	yt-live-chat-banner-manager,
	yt-live-chat-paid-message-renderer,
	yt-live-chat-membership-item-renderer,
	ytd-sponsorships-live-chat-gift-purchase-announcement-renderer,
	ytd-sponsorships-live-chat-gift-redemption-announcement-renderer,
	#ticker, #separator, #action-panel,
	#panel-pages, #input-panel, #chat-badges,
	#before-content-buttons {
		display: none !important;
	}

	/* --- Hide scrollbar --- */
	yt-live-chat-item-list-renderer #items,
	yt-live-chat-item-list-renderer #item-scroller {
		overflow: hidden !important;
	}

	/* --- Custom text message --- */
	yt-live-chat-text-message-renderer {
		font-size: 24px !important;
		padding: 5px 10px !important;
	}

	yt-live-chat-text-message-renderer yt-img-shadow {
		margin-right: 8px !important;
	}

	yt-live-chat-text-message-renderer yt-img-shadow img {
		width: 32px !important;
		height: 32px !important;
	}

	yt-live-chat-text-message-renderer #author-name,
	yt-live-chat-text-message-renderer #message {
		font-weight: 400;
		text-shadow:
			rgb(69, 69, 69) 3px 0px 0px,
			rgb(69, 69, 69) 2.83487px 0.981584px 0px,
			rgb(69, 69, 69) 2.35766px 1.85511px 0px,
			rgb(69, 69, 69) 1.62091px 2.52441px 0px,
			rgb(69, 69, 69) 0.705713px 2.91581px 0px,
			rgb(69, 69, 69) -0.287171px 2.98622px 0px,
			rgb(69, 69, 69) -1.24844px 2.72789px 0px,
			rgb(69, 69, 69) -2.07227px 2.16926px 0px,
			rgb(69, 69, 69) -2.66798px 1.37182px 0px,
			rgb(69, 69, 69) -2.96998px 0.42336px 0px,
			rgb(69, 69, 69) -2.94502px -0.571704px 0px,
			rgb(69, 69, 69) -2.59586px -1.50383px 0px,
			rgb(69, 69, 69) -1.96093px -2.27041px 0px,
			rgb(69, 69, 69) -1.11013px -2.78704px 0px,
			rgb(69, 69, 69) -0.137119px -2.99686px 0px,
			rgb(69, 69, 69) 0.850987px -2.87677px 0px,
			rgb(69, 69, 69) 1.74541px -2.43999px 0px,
			rgb(69, 69, 69) 2.44769px -1.73459px 0px,
			rgb(69, 69, 69) 2.88051px -0.838247px 0px;
	}
    ```

3. **Adjust Browser Source Settings**:
    - Set the width and height of the browser source to match your stream layout.
    - Ensure the "Shutdown source when not visible" option is unchecked to keep the chat connected even when switching scenes.

## Usage

With the custom CSS applied, your YouTube live chat will appear as a streamlined, transparent overlay in OBS, showing only the chat messages and highlighting messages from the owner. This setup is ideal for creating an engaging and visually appealing live stream.

## Contribution

Feel free to fork this repository and make your own adjustments. Pull requests are welcome if you have improvements or additional features you would like to add.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

Enjoy your clean and simple YouTube live chat overlay in OBS!
